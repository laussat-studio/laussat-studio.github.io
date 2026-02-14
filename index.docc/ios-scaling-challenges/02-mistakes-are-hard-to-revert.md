# Mistakes Are Hard to Revert

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-02-mistakes-are-hard-to-revert-icon.codex.svg", alt: "Mistakes are hard to revert Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-02-mistakes-are-hard-to-revert-card.codex.svg", alt: "Mistakes are hard to revert Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "ios-scaling-challenges-02-mistakes-are-hard-to-revert-hero.codex.svg", alt: "Mistakes are hard to revert Hero")

App Store review, phased release, and client rollout make hotfixes slow and
rollback paths narrow.

## Why it Gets Harder at Scale

- App Store propagation delays keep broken builds in the wild.
- Server flags cannot undo client regressions that ship in the binary.

## Scale Signals

- Incidents require server gating to mask client defects.
- Rollback plans are absent or untested in release playbooks.

## Laussat Studio Take

- Ship every change with a rollback story and a kill switch plan.

