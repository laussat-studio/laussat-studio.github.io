# DocC static hosting: baseUrl / `--hosting-base-path` (laussat.studio)

This doc exists because we lost time to a subtle but predictable failure mode: the site *loads* (HTTP 200) but renders a DocC **“Page not found”** UI due to a **hosting base path mismatch**.

It’s written as a practical runbook for maintaining `laussat.studio` and keeping it aligned with the known-good pattern used by `wrkstrm.com`.

---

## Glossary

### “DocC route”
A **page inside** the DocC SPA, e.g.:

- `/documentation/index/`
- `/documentation/some-symbol`

These are handled by DocC’s client-side router.

### “Hosting base path” / “baseUrl”
Where the **DocC SPA is mounted** on the website (the prefix for assets and the router).

- In the generated HTML, this appears as:

```html
<script>var baseUrl = "/"</script>
```

- In the build command, this is controlled by:

```sh
docc convert ... --transform-for-static-hosting --hosting-base-path <PATH>
```

**Key point:** Hosting base path is *not* the same thing as the DocC Technology Root or the route you want users to land on.

---

## Known-good target state (wrkstrm-style)

For `wrkstrm.com`, the DocC HTML at `https://wrkstrm.com/documentation/index/` shows:

- `baseUrl = "/"`
- assets load from `/<css|js|data>/...` (root)

We want the same for `laussat.studio`.

### Invariants

- DocC SPA **mounted at the domain root** (`baseUrl = "/"`).
- The human-friendly landing route is a DocC route:
  - `/` redirects to `/documentation/index/`.

---

## Symptoms of the base path mismatch

### Symptom A: “DocC page not found” UI but HTTP 200

A request like this returns HTTP 200:

- `GET /documentation/.../index/`

…but the page renders DocC’s “not found” screen.

This happens when the server returns the SPA shell (`index.html`) for many paths (so it’s 200), but the **client-side router** doesn’t have a matching route under the current `baseUrl`.

### Symptom B: blank page / missing CSS/JS

If `baseUrl` is `/` but the deployed files are still under a subdirectory, the app will request:

- `/js/...`
- `/css/...`

…and get 404s.

---

## Root cause (what went wrong historically)

`laussat.studio` was deployed with DocC built for a non-root base path. The generated HTML contained:

- `baseUrl = "/documentation/<tech-root>/"`

This meant:

- the DocC SPA expected to live at `/documentation/<tech-root>/`
- assets were referenced under `/documentation/<tech-root>/js/...`

…but the public URL policy we wanted was:

- `/documentation/index/` (one level deep after `/documentation`)

This mismatch caused:

- “not found” UI on a 200 response
- confusion because the network layer looked “healthy”

Fix was to align `--hosting-base-path` with `wrkstrm.com`:

- set `--hosting-base-path /`

Commit that did this (in this repo):

- `c07359a docc: set hosting-base-path to root (match wrkstrm)`

---

## How to verify (fast checks)

### 1) Inspect the generated HTML for `baseUrl`

```sh
curl -sS https://laussat.studio/documentation/index/ | grep -E "baseUrl|var baseUrl" | head
```

Expected:

- `var baseUrl = "/"`

### 2) Confirm assets exist at the expected mount

If `baseUrl = "/"`, then this must be 200:

```sh
curl -sSI https://laussat.studio/js/index.*.js | head
```

(Use the filename from the HTML if needed.)

### 3) Confirm redirect is correct

```sh
curl -sSI https://laussat.studio/ | sed -n '1,20p'
```

Expected:

- redirect/refresh to `/documentation/index/`

---

## Operational rules

### Rule 1: baseUrl must match where the artifact is served

- If artifact is served from root → `--hosting-base-path /`
- If artifact is served from `/something/` → `--hosting-base-path /something`

Do **not** try to “hack” the DocC route shape (e.g. `/documentation/index`) using `--hosting-base-path`. That flag changes **asset + router prefix**, not content routing rules.

### Rule 2: keep the workflow aligned with wrkstrm

When in doubt, diff the DocC publish workflow against the wrkstrm one:

- `wrkstrm.com`: `baseUrl = /`
- `laussat.studio`: should be the same

---

## Where the configuration lives

- GitHub Pages publish workflow:
  - `.github/workflows/publish.yml`

Look for the DocC build command:

```sh
docc convert "index.docc" \
  --output-path "${output_root}" \
  --transform-for-static-hosting \
  --hosting-base-path / \
  ...
```

---

## FAQ

### “But our Technology Root is `index.md`, doesn’t that force `/documentation/index`?”

No. Technology Root determines the **DocC landing page route** (inside the site), not the **hosting mount point**.

You can have:

- hosting mount: `/` (baseUrl `/`)
- landing route: `/documentation/index/`

and that’s the intended setup.
