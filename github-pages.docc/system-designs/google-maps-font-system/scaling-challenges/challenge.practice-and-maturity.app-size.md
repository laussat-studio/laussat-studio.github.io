# App size

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @PageImage(purpose: icon, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.app-size-icon.codex", alt: "App size icon")
  @PageImage(purpose: card, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.app-size-card.codex", alt: "App size card")
}

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.app-size-hero.codex", alt: "App size hero")

This page records how the Google Maps typography system addressed "App size".

## Challenge

We had to ensure bundle size would not increase.

## System design response

We created a report showing the font was present with and without the feature.

## Evidence and remaining risk

Evidence: no app size gain. We created size reports with experimentation
toggled on/off at compile time.
## Diagram: Context snapshot

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.app-size-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.app-size-context.svg
%% title: App size - Context snapshot
flowchart LR
  A["Challenge: App size"] --> B["Constraint or pressure"]
  B --> C["System design response"]
  C --> D["Evidence and remaining risk"]
```
