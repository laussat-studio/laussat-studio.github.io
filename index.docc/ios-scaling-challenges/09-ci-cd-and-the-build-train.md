# CI and the Build Train

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-09-ci-cd-and-the-build-train-icon.codex.svg", alt: "CI and the build train Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-09-ci-cd-and-the-build-train-card.codex.svg", alt: "CI and the build train Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-09-ci-cd-and-the-build-train-hero.codex.svg", alt: "CI and the build train Hero")

Code signing, provisioning, and Xcode tooling make mobile release pipelines more
fragile.

## Why it Gets Harder at Scale

- Build reproducibility depends on exact toolchain and signing state.
- TestFlight and App Store gating introduce non-engineering delays.

## Scale Signals

- CI pipelines fail on signing or provisioning drift.
- Release candidates stall due to slow validation cycles.

## Laussat Studio Take

- Automate signing and document promotion rules for each train.

## Diagram: Context Snapshot

@Image(source: "ios-scaling-challenges-09-ci-cd-and-the-build-train-context.mermaid.svg", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-09-ci-cd-and-the-build-train-context.svg
%% title: CI and the build train - Context snapshot
flowchart LR
  A["CI and the build train"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
