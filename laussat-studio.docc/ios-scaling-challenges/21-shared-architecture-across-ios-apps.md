# Shared architecture across iOS apps

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-21-shared-architecture-across-ios-apps-icon.codex", alt: "Shared architecture across iOS apps Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-21-shared-architecture-across-ios-apps-card.codex", alt: "Shared architecture across iOS apps Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "doc-21-shared-architecture-across-ios-apps-hero.codex", alt: "Shared architecture across iOS apps hero")

@Image(source: "ios-scaling-challenges-21-shared-architecture-across-ios-apps-hero.codex", alt: "Shared architecture across iOS apps Hero")

Shared SDKs and design systems can scale a portfolio, but only with careful
versioning.

## Why it gets harder at scale

- Internal SDKs must support multiple release cadences.
- Migration tooling is required to avoid breaking dependent apps.

## Scale signals

- Shared libraries block releases due to incompatible changes.
- Teams fork shared modules to avoid upgrades.

## Studio Laussat take

- Use semantic versioning and adapters for backward compatibility.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-21-shared-architecture-across-ios-apps-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-21-shared-architecture-across-ios-apps-context.svg
%% title: Shared architecture across iOS apps - Context snapshot
flowchart LR
  A["Shared architecture across iOS apps"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```