# Requirements and Constraints

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Requirements and Constraints")
  @PageImage(purpose: icon, source: "system-designs-system-design-dimensions-dimensions-requirements-and-constraints-icon.codex", alt: "Requirements and Constraints icon")
  @PageImage(purpose: card, source: "system-designs-system-design-dimensions-dimensions-requirements-and-constraints-card.codex", alt: "Requirements and Constraints card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "system-designs-system-design-dimensions-dimensions-requirements-and-constraints-hero.codex", alt: "Requirements and Constraints hero")

Capture the technical and organizational guardrails.

## Include

- Functional requirements.
- Non-functional constraints (latency, cost, offline, accessibility).
- Organizational constraints (teams, timelines, dependencies).

## Diagram: Context snapshot

@Image(source: "system-designs-system-design-dimensions-dimensions-requirements-and-constraints-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: system-designs-system-design-dimensions-dimensions-requirements-and-constraints-context.svg
%% title: Requirements and Constraints - Context snapshot
flowchart LR
  A["Requirements and Constraints"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```