# Stakeholders and Ownership

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Stakeholders and Ownership")
  @PageImage(purpose: icon, source: "system-designs-icon.codex.svg", alt: "Stakeholders and Ownership icon")
  @PageImage(purpose: card, source: "system-designs-card.codex.svg", alt: "Stakeholders and Ownership card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "index-hero.codex.svg", alt: "Stakeholders and Ownership hero")

## Primary User

- YouTube Shorts creators.

## Ownership

- Feature design and shipping ownership: iOS.
- Client-side responsibilities: interaction loop, caching, on-device composition.
- Server-side dependency: backend AI audio generation endpoint.

## Partner Surfaces

- Experimentation platform for staged rollout.
- Infrastructure and backend teams for generation services.
- Policy/compliance stakeholders for allowed content boundaries.
