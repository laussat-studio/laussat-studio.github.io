# Client-side data migrations

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-37-client-side-data-migrations-icon.codex", alt: "Client-side data migrations Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-37-client-side-data-migrations-card.codex", alt: "Client-side data migrations Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "doc-37-client-side-data-migrations-hero.codex", alt: "Client side data migrations hero")

@Image(source: "ios-scaling-challenges-37-client-side-data-migrations-hero.codex", alt: "Client-side data migrations Hero")

Core Data and SQLite migrations require careful versioning and testing.

## Why it gets harder at scale

- Schema drift across releases complicates migration paths.
- Large datasets make migrations slow or fragile.

## Scale signals

- Upgrade crashes spike after migrations ship.
- Users report data loss or missing records.

## Studio Laussat take

- Test migrations against historical snapshots and large data sets.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-37-client-side-data-migrations-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-37-client-side-data-migrations-context.svg
%% title: Client-side data migrations - Context snapshot
flowchart LR
  A["Client-side data migrations"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```