# Cross-platform vs Native Decision Framework

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-28-cross-platform-vs-native-decision-framework-icon.codex", alt: "Cross-platform vs native decision framework Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-28-cross-platform-vs-native-decision-framework-card.codex", alt: "Cross-platform vs native decision framework Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-28-cross-platform-vs-native-decision-framework-hero.codex", alt: "Cross-platform vs native decision framework Hero")

Choosing React Native, WebView, or native has long-term product implications.

## Why It Gets Harder at Scale

- Shared stacks can slow platform-specific performance tuning.
- Debugging toolchains multiply when stacks diverge.

## Scale Signals

- Performance regressions persist due to stack limitations.
- Feature delivery slows as teams negotiate ownership.

## Laussat Studio Take

- Use a decision rubric that weighs performance, UX, and maintenance cost.

## Diagram: Context Snapshot

@Image(source: "ios-scaling-challenges-28-cross-platform-vs-native-decision-framework-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-28-cross-platform-vs-native-decision-framework-context.svg
%% title: Cross-platform vs native decision framework - Context snapshot
flowchart LR
  A["Cross-platform vs native decision framework"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
