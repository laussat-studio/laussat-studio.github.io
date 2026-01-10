# Experimentation

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-30-experimentation-icon.codex", alt: "Experimentation Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-30-experimentation-card.codex", alt: "Experimentation Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-30-experimentation-hero.codex", alt: "Experimentation Hero")

Experimentation requires careful rollout, measurement, and guardrails.

## Why it gets harder at scale

- Client-side flag evaluation can drift from server expectations.
- Long release cycles delay feedback loops.

## Scale signals

- Metrics are inconclusive due to inconsistent flag targeting.
- Experiments outlive their learning goals.

## Studio Laussat take

- Use explicit guardrails and experiment lifecycles.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-30-experimentation-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-30-experimentation-context.svg
%% title: Experimentation - Context snapshot
flowchart LR
  A["Experimentation"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
