# Architecting to avoid collisions

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @PageImage(purpose: icon, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.large-ios-teams.architecting-to-avoid-collisions-icon.codex", alt: "Architecting to avoid collisions icon")
  @PageImage(purpose: card, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.large-ios-teams.architecting-to-avoid-collisions-card.codex", alt: "Architecting to avoid collisions card")
}

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.large-ios-teams.architecting-to-avoid-collisions-hero.codex", alt: "Architecting to avoid collisions hero")

This page records how the Google Maps typography system addressed "Architecting to avoid collisions".

## Challenge

For colors, state was passed at the controller level, which required handing
values off between controllers and increased collision risk.

## System design response

For fonts, we moved state to a base service level and provided a single API
surface for developers to use.

## Evidence and remaining risk

Evidence: all old APIs were wrapped around the new API protocol.
## Diagram: Context snapshot

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.large-ios-teams.architecting-to-avoid-collisions-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: system-designs-google-maps-font-system-scaling-challenges-challenge.large-ios-teams.architecting-to-avoid-collisions-context.svg
%% title: Architecting to avoid collisions - Context snapshot
flowchart LR
  A["Challenge: Architecting to avoid collisions"] --> B["Constraint or pressure"]
  B --> C["System design response"]
  C --> D["Evidence and remaining risk"]
```
