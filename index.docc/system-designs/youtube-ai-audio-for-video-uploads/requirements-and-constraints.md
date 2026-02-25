# Requirements and Constraints

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Requirements and Constraints")
  @PageImage(purpose: icon, source: "requirements-and-constraints-icon.codex.svg", alt: "Requirements and Constraints icon")
  @PageImage(purpose: card, source: "requirements-and-constraints-card.codex.svg", alt: "Requirements and Constraints card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "requirements-and-constraints-hero.codex.svg", alt: "Requirements and Constraints hero")

## Requirements

- Primary flow had to support YouTube Shorts creators.
- Creator could choose from 5 voices.
- Composition had to support up to 20 concurrent audio stickers.
- Language detection decisions needed to happen on each keystroke.
- Network requests were debounced to 3 seconds during typing.
- Language detection latency target was under 1 second.
- Audio generation happened in backend services.
- Audio mixing and composition happened on device.
- Rollout had to run via experiment with crash monitoring.

## Constraints

- English only.
- Content policy guardrails included curse word handling and emoji exclusions.
- Existing infrastructure had operational and integration friction points.
- UI complexity increased due to variable text and expanded action/menu surfaces.
