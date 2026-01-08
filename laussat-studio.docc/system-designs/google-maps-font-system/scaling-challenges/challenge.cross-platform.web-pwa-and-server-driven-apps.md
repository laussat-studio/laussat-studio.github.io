# Web, PWA, and server-driven apps

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @PageImage(purpose: icon, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.web-pwa-and-server-driven-apps-icon.codex", alt: "Web, PWA, and server-driven apps icon")
  @PageImage(purpose: card, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.web-pwa-and-server-driven-apps-card.codex", alt: "Web, PWA, and server-driven apps card")
}

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.web-pwa-and-server-driven-apps-hero.codex", alt: "Web, PWA, and server-driven apps hero")

This page records how the Google Maps typography system addressed "Web, PWA, and server-driven apps".

## Challenge

Web teams handled these APIs for server-driven and web surfaces.

## System design response

We rejected this path due to performance.

## Evidence and remaining risk

N/A.
## Diagram: Context snapshot

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.web-pwa-and-server-driven-apps-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.web-pwa-and-server-driven-apps-context.svg
%% title: Web, PWA, and server-driven apps - Context snapshot
flowchart LR
  A["Challenge: Web, PWA, and server-driven apps"] --> B["Constraint or pressure"]
  B --> C["System design response"]
  C --> D["Evidence and remaining risk"]
```
