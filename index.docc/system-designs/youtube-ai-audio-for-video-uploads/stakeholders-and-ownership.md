# Stakeholders and Ownership

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Stakeholders and Ownership")
  @PageImage(purpose: icon, source: "stakeholders-and-ownership-icon.codex.svg", alt: "Stakeholders and Ownership icon")
  @PageImage(purpose: card, source: "stakeholders-and-ownership-card.codex.svg", alt: "Stakeholders and Ownership card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "stakeholders-and-ownership-hero.codex.svg", alt: "Stakeholders and Ownership hero")

## Primary user

- YouTube Shorts creators.

## Ownership (who built what)

- iOS owned feature design + shipping.
- Client responsibilities: the editor loop, caching policy, and accessibility.
- Server dependency: the AI audio generation endpoint (synthesis + response format).

## Partner surfaces (who we depended on)

- Experimentation platform for staged rollout and monitoring.
- Backend/infrastructure teams for generation services reliability and scale.
- Policy/compliance for content boundaries (what we allow, what we block).
