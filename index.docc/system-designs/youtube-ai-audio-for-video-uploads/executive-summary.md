# Executive Summary

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Executive Summary")
  @PageImage(purpose: icon, source: "executive-summary-icon.codex.svg", alt: "Executive Summary icon")
  @PageImage(purpose: card, source: "executive-summary-card.codex.svg", alt: "Executive Summary card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "executive-summary-hero.codex.svg", alt: "Executive Summary hero")

YouTube Shorts creators needed quick narration without recording their own voice. We shipped AI voiceover for text stickers on iOS: pick one of five voices, type, and hear narration immediately — while supporting up to 20 concurrent audio tracks in a single composition.

Key technical outcomes:

- Keystroke loop with language detection, plus caching to avoid repeat work and reduce duplicate synthesis.
- Long-term caching that persists beyond the upload flow (post-video upload) for repeat text/voice patterns.
- Experiments are allowed to collide during the beta period — better to surface feature-mix breakage there than in production.
