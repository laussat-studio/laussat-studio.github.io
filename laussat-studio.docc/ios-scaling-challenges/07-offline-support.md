# Offline support

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-07-offline-support-icon.codex", alt: "Offline support Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-07-offline-support-card.codex", alt: "Offline support Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-07-offline-support-hero.codex", alt: "Offline support Hero")

Offline experiences demand durable persistence, conflict resolution, and clear
sync rules.

## Why it gets harder at scale

- Multiple stores and caches drift without a single source of truth.
- Background sync limitations amplify stale data and conflicts.

## Scale signals

- Users see stale content after reconnecting.
- Retry queues grow without deterministic resolution.

## Studio Laussat take

- Build an offline state machine with explicit sync stages.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-07-offline-support-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-07-offline-support-context.codex.svg
%% title: Offline support - Context snapshot
flowchart LR
  A["Offline support"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
