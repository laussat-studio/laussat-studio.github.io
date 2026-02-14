# Long Tail of Old App Versions

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-03-long-tail-of-old-app-versions-icon.codex.svg", alt: "Long tail of old app versions Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-03-long-tail-of-old-app-versions-card.codex.svg", alt: "Long tail of old app versions Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "ios-scaling-challenges-03-long-tail-of-old-app-versions-hero.codex.svg", alt: "Long tail of old app versions Hero")

Real adoption curves mean you support multiple OS and app versions long after a
release ships.

## Why it Gets Harder at Scale

- Back-deployed APIs and availability checks fragment code paths.
- Server contracts must remain compatible with older client behavior.

## Scale Signals

- Feature logic branches by OS and app version throughout the codebase.
- API changes require long compatibility windows and duplicated paths.

## Laussat Studio Take

- Maintain a capabilities matrix and plan deprecations in advance.

