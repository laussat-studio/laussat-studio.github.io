# Cross-platform Feature Development

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-27-cross-platform-feature-development-icon.codex.svg", alt: "Cross-platform feature development Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-27-cross-platform-feature-development-card.codex.svg", alt: "Cross-platform feature development Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "ios-scaling-challenges-27-cross-platform-feature-development-hero.codex.svg", alt: "Cross-platform feature development Hero")

Feature parity across platforms requires shared contracts without shared UI.

## Why it Gets Harder at Scale

- Inconsistent server models lead to divergent client behavior.
- Testing parity requires shared fixtures and specs.

## Scale Signals

- iOS behavior drifts from web or Android experiences.
- API changes break one platform at a time.

## Laussat Studio Take

- Use shared schemas and contract tests to keep parity.

## Diagram: Context Snapshot
