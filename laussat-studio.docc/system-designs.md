# System designs

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Implemented Systems")
  @PageImage(purpose: icon, source: "system-designs-icon.codex", alt: "System designs Icon")
  @PageImage(purpose: card, source: "system-designs-card.codex", alt: "System designs Card")
}

@Options {
  @TopicsVisualStyle(detailedGrid)
  @AutomaticSeeAlso(disabled)
}

@Image(source: "system-designs-hero.codex", alt: "System designs Hero")

A library of prior work case studies: system designs that shipped in production
and were refined under real‑world constraints.

@Image(source: "laussat-studio-hero.codex", alt: "Studio Laussat Hero")


## Topics

- <doc:system-design-dimensions>
- <doc:google-maps-typography-design-overview>

## Diagram: Context snapshot

@Image(source: "system-designs-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: system-designs-context.svg
%% title: System designs - Context snapshot
flowchart LR
  A["System designs"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
