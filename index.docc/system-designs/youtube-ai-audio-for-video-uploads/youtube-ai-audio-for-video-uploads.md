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

Most of the bugs weren’t about the new feature — they came from older systems that needed to be optimized, and from experiments colliding with each other. That collision is an intended part of the release process: we want feature mixes to break in controlled environments so they don’t inadvertently break the production version. As the number of audio tracks increased, we tightened timeline ordering logic in legacy components so previews stayed instant and exports stayed correct.

## Product Summary

| Attribute | Details |
|---|---|
| Primary user | YouTube Shorts creators |
| Client ownership | iOS |
| Input loop | Language detection on every keystroke |
| Network cadence | Debounced synthesis requests (~3s) while typing |
| Generation | Backend audio synthesis |
| Composition | On-device mixdown into the video timeline |
| Scale target | Up to 20 concurrent audio stickers; 5 voice options |
| Language scope | English only (v1) |

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
