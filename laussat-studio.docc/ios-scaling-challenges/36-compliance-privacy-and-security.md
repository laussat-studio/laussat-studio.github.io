# Compliance, privacy, and security

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-36-compliance-privacy-and-security-icon.codex", alt: "Compliance, privacy, and security Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-36-compliance-privacy-and-security-card.codex", alt: "Compliance, privacy, and security Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-36-compliance-privacy-and-security-hero.codex", alt: "Compliance, privacy, and security Hero")

Privacy manifests, ATT, and secure storage require disciplined governance.

## Why it gets harder at scale

- Data flows shift faster than privacy disclosures are updated.
- Platform policies change annually, forcing urgent updates.

## Scale signals

- App Store review rejections for privacy or tracking.
- Logging includes sensitive data unintentionally.

## Studio Laussat take

- Include privacy review gates in release workflows.

## Diagram: Context snapshot

@Image(source: "ios-scaling-challenges-36-compliance-privacy-and-security-context.mermaid", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-36-compliance-privacy-and-security-context.svg
%% title: Compliance, privacy, and security - Context snapshot
flowchart LR
  A["Compliance, privacy, and security"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
