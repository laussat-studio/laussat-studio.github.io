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

- The primary flow had to work for YouTube Shorts creators — fast, in-editor, no friction.
- Creators needed 5 voice options.
- The composition had to support up to 10 concurrent audio stickers.
- Language detection had to run on every keystroke (the editor loop).
- Network synthesis requests were debounced to 3 seconds so the user isn’t surprised by voice playback firing too quickly while typing.
- Audio synthesis happens in backend services.
- Mixing and composition happen on-device.
- Rollout had to run as an experiment with crash monitoring and fast rollback.

## Constraints

- English only (v1). At first thought, shipping only English would seem to make the task easier, but it made the feature harder. On-device language detection gets messy in real editing: detecting Spanish mid-sentence could remove a voice from the composition, then enable it again several keystrokes later.
- Content policy guardrails: curse word handling and emoji exclusions.
- Existing infrastructure had real operational/integration friction.
- UI complexity was unavoidable: variable text plus expanded menus/action surfaces increased both layout risk and composition risk.
