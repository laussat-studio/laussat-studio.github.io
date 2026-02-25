# Migration Details

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Migration Details")
  @PageImage(purpose: icon, source: "system-designs-icon.codex.svg", alt: "Migration Details icon")
  @PageImage(purpose: card, source: "system-designs-card.codex.svg", alt: "Migration Details card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "index-hero.codex.svg", alt: "Migration Details hero")

## Baseline to New Flow

Before:

- Audio overlap and menu option growth were not primary design assumptions.
- Existing pipeline behavior and UI systems were not tuned for generated voice variation.

After:

- Pipeline supported per-keystroke local decisions plus debounced generation requests.
- Composition flow supported up to 20 concurrent audio tracks.
- Persistent cache path supported repeated voice/text CTA patterns.

## Migration Notes

- UI breakdowns under expanded options were a recurring implementation challenge.
- Infrastructure behavior required iterative adaptation during integration and experiment phases.
