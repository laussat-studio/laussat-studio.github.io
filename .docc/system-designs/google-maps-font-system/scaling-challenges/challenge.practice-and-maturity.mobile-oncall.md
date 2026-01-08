# Mobile oncall

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @PageImage(purpose: icon, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.mobile-oncall-icon.codex", alt: "Mobile oncall icon")
  @PageImage(purpose: card, source: "system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.mobile-oncall-card.codex", alt: "Mobile oncall card")
}

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.mobile-oncall-hero.codex", alt: "Mobile oncall hero")

This page records how the Google Maps typography system addressed "Mobile oncall".

## Challenge

Mobile on-call needed a clear escalation path for typography changes.

## System design response

We had SRE coverage for on-call support.

## Evidence and remaining risk

Evidence: no incidents were reported.

## Diagram: Context snapshot

@Image(source: "system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.mobile-oncall-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: system-designs-google-maps-font-system-scaling-challenges-challenge.practice-and-maturity.mobile-oncall-context.svg
%% title: Mobile oncall - Context snapshot
flowchart LR
  A["Challenge: Mobile oncall"] --> B["Constraint or pressure"]
  B --> C["System design response"]
  C --> D["Evidence and remaining risk"]
```
