# Cross-platform feature development

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @PageImage(purpose: icon, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.cross-platform-feature-development-icon.codex", alt: "Cross-platform feature development icon")
  @PageImage(purpose: card, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.cross-platform-feature-development-card.codex", alt: "Cross-platform feature development card")
}

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.cross-platform-feature-development-hero.codex", alt: "Cross-platform feature development hero")

This page records how the Google Maps typography system addressed "Cross-platform feature development".

## Challenge

iPad vs iPhone were on two different timelines, so they needed separate
experiment setups.

## System design response

We kept both surfaces stable throughout the transition.

## Evidence and remaining risk

iPhone and iPad shipped two design systems at the same time.
## Diagram: Context snapshot

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.cross-platform-feature-development-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: system-designs-google-maps-font-system-scaling-challenges-challenge.cross-platform.cross-platform-feature-development-context.svg
%% title: Cross-platform feature development - Context snapshot
flowchart LR
  A["Challenge: Cross-platform feature development"] --> B["Constraint or pressure"]
  B --> C["System design response"]
  C --> D["Evidence and remaining risk"]
```
