# In-app Purchases

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-12-in-app-purchases-icon.codex", alt: "In-app purchases Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-12-in-app-purchases-card.codex", alt: "In-app purchases Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-12-in-app-purchases-hero.codex", alt: "In-app purchases Hero")

StoreKit subscriptions and entitlements require strict modeling and verification.

## Why it Gets Harder at Scale

- Subscription states change asynchronously across devices.
- Receipt validation needs server enforcement to prevent drift.

## Scale Signals

- Users see entitlement mismatches across devices.
- Restore flows behave inconsistently across cohorts.

## Laussat Studio Take

- Treat entitlements as server-verified state, not client truth.

## Diagram: Context Snapshot

@Image(source: "ios-scaling-challenges-12-in-app-purchases-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-12-in-app-purchases-context.svg
%% title: In-app purchases - Context snapshot
flowchart LR
  A["In-app purchases"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
