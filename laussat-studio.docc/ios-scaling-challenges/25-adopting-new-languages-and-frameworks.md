# Adopting new languages and frameworks

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-25-adopting-new-languages-and-frameworks-icon.codex", alt: "Adopting new languages and frameworks Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-25-adopting-new-languages-and-frameworks-card.codex", alt: "Adopting new languages and frameworks Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-25-adopting-new-languages-and-frameworks-hero.codex", alt: "Adopting new languages and frameworks Hero")

Swift language updates and SwiftUI adoption require staged migration strategy.

## Why it gets harder at scale

- Mixed paradigms create uneven architecture and training gaps.
- Concurrency changes can introduce new correctness requirements.

## Scale signals

- Teams fork patterns for the same UI problems.
- Migration work blocks roadmap commitments.

## Studio Laussat take

- Use staged migrations with playbooks and training checkpoints.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-25-adopting-new-languages-and-frameworks-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-25-adopting-new-languages-and-frameworks-context.svg
%% title: Adopting new languages and frameworks - Context snapshot
flowchart LR
  A["Adopting new languages and frameworks"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
