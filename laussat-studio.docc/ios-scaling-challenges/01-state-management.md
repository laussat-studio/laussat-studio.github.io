# State management

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-01-state-management-icon.codex", alt: "State management Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-01-state-management-card.codex", alt: "State management Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "doc-01-state-management-hero.codex", alt: "State management hero")

@Image(source: "ios-scaling-challenges-01-state-management-hero.codex", alt: "State management Hero")

Large iOS apps juggle UIKit and SwiftUI lifecycles, async state, and multiple
stores of truth.

## Why it gets harder at scale

- Multiple entry points fight over ownership of state and navigation.
- MainActor boundaries and reentrancy make subtle bugs hard to reproduce.

## Scale signals

- UI desync between tabs, scenes, or deep link entry paths.
- Frequent "state reset" bugs after background or cold start.

## Studio Laussat take

- Define a single state graph per feature and enforce ownership.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-01-state-management-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-01-state-management-context.codex.svg
%% title: State management - Context snapshot
flowchart LR
  A["State management"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```