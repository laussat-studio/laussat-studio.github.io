# Push and background notifications

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-05-push-and-background-notifications-icon.codex", alt: "Push and background notifications Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-05-push-and-background-notifications-card.codex", alt: "Push and background notifications Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "doc-05-push-and-background-notifications-hero.codex", alt: "Push and background notifications hero")

@Image(source: "ios-scaling-challenges-05-push-and-background-notifications-hero.codex", alt: "Push and background notifications Hero")

APNs delivery is best-effort, and background work is constrained by OS policy.

## Why it gets harder at scale

- Silent pushes and background tasks are throttled unpredictably.
- Background URL sessions and refresh windows vary by device state.

## Scale signals

- Background sync success rates fluctuate across cohorts.
- Users report missing updates despite correct server behavior.

## Studio Laussat take

- Design idempotent background work with explicit retry queues.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-05-push-and-background-notifications-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-05-push-and-background-notifications-context.codex.svg
%% title: Push and background notifications - Context snapshot
flowchart LR
  A["Push and background notifications"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```