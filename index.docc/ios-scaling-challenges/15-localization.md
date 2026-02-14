# Localization

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-15-localization-icon.codex.svg", alt: "Localization Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-15-localization-card.codex.svg", alt: "Localization Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "ios-scaling-challenges-15-localization-hero.codex.svg", alt: "Localization Hero")

Localization expands layout and can destabilize UI when strings grow.

## Why it Gets Harder at Scale

- String catalogs and pluralization rules are easy to fragment.
- Right-to-left and accessibility sizes amplify layout issues.

## Scale Signals

- Truncation and clipping appear in secondary locales.
- UI test coverage misses localized regressions.

## Laussat Studio Take

- Use pseudo-localization and RTL testing in CI.

