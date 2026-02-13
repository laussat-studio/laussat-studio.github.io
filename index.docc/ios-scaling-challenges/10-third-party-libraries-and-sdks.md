# Third-party Libraries and SDKs

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-10-third-party-libraries-and-sdks-icon.codex.svg", alt: "Third-party libraries and SDKs Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-10-third-party-libraries-and-sdks-card.codex.svg", alt: "Third-party libraries and SDKs Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "ios-scaling-challenges-10-third-party-libraries-and-sdks-hero.codex.svg", alt: "Third-party libraries and SDKs Hero")

SDK sprawl affects startup time, privacy posture, and update cadence.

## Why it Gets Harder at Scale

- Binary frameworks hide behavior and can introduce swizzling risks.
- Vendor release cycles rarely align with App Store schedules.

## Scale Signals

- App startup time grows with each new SDK.
- Privacy manifests and data flows drift out of compliance.

## Laussat Studio Take

- Wrap third-party SDKs behind internal adapters and version them.

## Diagram: Context Snapshot
