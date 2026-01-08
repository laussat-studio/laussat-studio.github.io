# Deeplinks and routing

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-04-deeplinks-and-routing-icon.codex", alt: "Deeplinks and routing Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-04-deeplinks-and-routing-card.codex", alt: "Deeplinks and routing Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "doc-04-deeplinks-and-routing-hero.codex", alt: "Deeplinks and routing hero")

@Image(source: "ios-scaling-challenges-04-deeplinks-and-routing-hero.codex", alt: "Deeplinks and routing Hero")

Universal Links, custom schemes, and scene lifecycles make deep links brittle at
scale.

## Why it gets harder at scale

- Cold start and warm start flows diverge across scenes and tabs.
- Attribution and logging need to survive auth gates and delayed routing.

## Scale signals

- Deep links work in some entry paths but fail in others.
- Attribution and routing metrics are missing or inconsistent.

## Studio Laussat take

- Centralize routing and log every deep link decision path.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-04-deeplinks-and-routing-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-04-deeplinks-and-routing-context.codex.svg
%% title: Deeplinks and routing - Context snapshot
flowchart LR
  A["Deeplinks and routing"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```