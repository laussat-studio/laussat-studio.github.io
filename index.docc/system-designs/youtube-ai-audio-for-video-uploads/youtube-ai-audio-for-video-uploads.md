# YouTube AI Audio for Video Uploads

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("YouTube AI Audio for Video Uploads")
  @PageImage(purpose: icon, source: "system-designs-icon.codex.svg", alt: "YouTube AI Audio for Video Uploads icon")
  @PageImage(purpose: card, source: "system-designs-card.codex.svg", alt: "YouTube AI Audio for Video Uploads card")
}

@Options {
  @TopicsVisualStyle(detailedGrid)
  @AutomaticSeeAlso(disabled)
}

A case study on shipping AI-powered audio sticker narration for YouTube Shorts uploads.

@Image(source: "index-hero.codex.svg", alt: "YouTube AI Audio for Video Uploads hero")

Creators wanted a fast way to narrate sticker text without recording their own voice. The product direction was to improve upload quality and encourage more sharing by letting creators choose one of five voices and preview audio while writing.

Implementation ran for one quarter, followed by one quarter of experimentation.

## Product Summary

- Primary user: YouTube Shorts creators.
- Client ownership: iOS.
- Input loop: local language detection decisions on each keystroke.
- Network cadence: debounced requests at 3 seconds while typing.
- Generation: backend AI audio synthesis.
- Composition: on-device audio mixing into video.
- Scale target: up to 20 concurrent audio stickers, 5 available voices.
- Language scope: English only.

## Pipeline

Text input -> language detection -> debounced network request -> network response -> audio cache -> save audio -> merge into video -> prepare upload -> upload.

## Topics

- <doc:executive-summary>
- <doc:problem-context>
- <doc:requirements-and-constraints>
- <doc:stakeholders-and-ownership>
- <doc:strategy-and-execution>
- <doc:rollout-and-results>
- <doc:lessons>
- <doc:migration-details>
- <doc:deep-dive-expectations>
- <doc:open-questions>
