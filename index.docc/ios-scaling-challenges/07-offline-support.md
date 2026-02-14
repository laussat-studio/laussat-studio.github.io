# Offline Support

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-07-offline-support-icon.codex.svg", alt: "Offline support Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-07-offline-support-card.codex.svg", alt: "Offline support Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "ios-scaling-challenges-07-offline-support-hero.codex.svg", alt: "Offline support Hero")

Offline experiences demand durable persistence, conflict resolution, and clear
sync rules.

## Why it Gets Harder at Scale

- Multiple stores and caches drift without a single source of truth.
- Background sync limitations amplify stale data and conflicts.

## Scale Signals

- Users see stale content after reconnecting.
- Retry queues grow without deterministic resolution.

## Laussat Studio Take

- Build an offline state machine with explicit sync stages.

