# Tooling maturity for large iOS teams

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-22-tooling-maturity-for-large-ios-teams-icon.codex", alt: "Tooling maturity for large iOS teams Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-22-tooling-maturity-for-large-ios-teams-card.codex", alt: "Tooling maturity for large iOS teams Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-22-tooling-maturity-for-large-ios-teams-hero.codex", alt: "Tooling maturity for large iOS teams Hero")

Large teams need consistent linting, documentation, and metrics to scale.

## Why it gets harder at scale

- Tooling decisions drift by team and codebase.
- Metrics are missing or inconsistent across surfaces.

## Scale signals

- Style and lint baselines differ across modules.
- Build and test metrics are not tracked or visible.

## Studio Laussat take

- Provide a paved road for linting, docs, and performance budgets.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-22-tooling-maturity-for-large-ios-teams-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-22-tooling-maturity-for-large-ios-teams-context.svg
%% title: Tooling maturity for large iOS teams - Context snapshot
flowchart LR
  A["Tooling maturity for large iOS teams"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
