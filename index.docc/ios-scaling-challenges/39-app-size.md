# App Size

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-39-app-size-icon.codex.svg", alt: "App size Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-39-app-size-card.codex.svg", alt: "App size Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "ios-scaling-challenges-39-app-size-hero.codex.svg", alt: "App size Hero")

Binary size grows with assets, duplicate frameworks, and unused code paths.

## Why it Gets Harder at Scale

- Asset catalogs and bundles expand faster than cleanup.
- Static linking and generics can bloat binaries.

## Scale Signals

- App size increases every release without explanation.
- Downloads drop in low-bandwidth regions.

## Laussat Studio Take

- Audit size budgets and use on-demand resources.

## Diagram: Context Snapshot
