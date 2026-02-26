# Lessons

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Lessons")
  @PageImage(purpose: icon, source: "lessons-icon.codex.svg", alt: "Lessons icon")
  @PageImage(purpose: card, source: "lessons-card.codex.svg", alt: "Lessons card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "lessons-hero.codex.svg", alt: "Lessons hero")

## Key lessons

- The AI API was the easy part. Shipping the feature was everything around it: editor loop, caching, composition, and rollout.
- Caching + request shaping isn’t “optimization” — it changes cost, latency, and whether the feature feels reliable.
- As soon as audio overlap increased, hidden assumptions became bottlenecks which had to be addressed.
- Experiments and rollback aren’t release chores; they’re architecture. If you don’t design for collisions, production will do it for you.

## Operational insight

AI is an amazing API that can generate almost any content you want. But the API is 10% of any feature I’ve ever worked on. The other 90% is the experience.
