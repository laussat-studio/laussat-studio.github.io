# YouTube AI Audio for Video Uploads

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("YouTube AI Audio for Video Uploads")
  @PageImage(purpose: icon, source: "youtube-ai-audio-for-video-uploads-icon.codex.svg", alt: "YouTube AI Audio for Video Uploads icon")
  @PageImage(purpose: card, source: "youtube-ai-audio-for-video-uploads-card.codex.svg", alt: "YouTube AI Audio for Video Uploads card")
}

@Options {
  @TopicsVisualStyle(detailedGrid)
  @AutomaticSeeAlso(disabled)
}

A case study on shipping AI-powered audio sticker narration for YouTube Shorts uploads.

@Image(source: "youtube-ai-audio-for-video-uploads-hero.codex.svg", alt: "YouTube AI Audio for Video Uploads hero")

TikTok popularized AI voiceovers for text stickers overlaid on short-form video. It’s a quintessential feature for any app trying to compete in the space. This project focused on letting creators choose one of five voices and preview narration while writing — for that instant feedback and gratification.

After shipping, we iterated on the loop: audio quality, perceived latency, and the edge cases that only show up once creators start using it at scale.

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
