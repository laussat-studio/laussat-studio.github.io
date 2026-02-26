# Problem Context

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Problem Context")
  @PageImage(purpose: icon, source: "problem-context-icon.codex.svg", alt: "Problem Context icon")
  @PageImage(purpose: card, source: "problem-context-card.codex.svg", alt: "Problem Context card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "problem-context-hero.codex.svg", alt: "Problem Context hero")

Creators were already using text stickers as a narration workaround — because a lot of people don’t want to record their own voice. The problem is that voice is time: recording breaks the upload flow. So the upload experience had to keep momentum while creators typed, picked a voice, and previewed generated audio in real time.

Before this project:

- The audio pipeline wasn’t built for this variety of generated sounds showing up mid-edit.
- Earlier versions assumed low overlap: a few sounds, rarely concurrent, and mostly one at a time.
- UI and composition complexity had crept up: menu surfaces grew from 1–2 options to multiple variable-length options, which made both layout and mixing logic easier to break.

Business intent:

- Improve the quality of Shorts uploads.
- Encourage more creator sharing activity.
- Keep interaction responsiveness tight during authoring — without losing a frame.
