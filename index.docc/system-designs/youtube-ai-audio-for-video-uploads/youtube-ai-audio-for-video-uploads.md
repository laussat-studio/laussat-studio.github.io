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

A case study on shipping AI voiceover for text stickers in YouTube Shorts uploads — turning keystrokes into stories, without losing a frame.

@Image(source: "youtube-ai-audio-for-video-uploads-hero.codex.svg", alt: "YouTube AI Audio for Video Uploads hero")

TikTok made AI voiceovers on text stickers feel inevitable in short-form video. For any app competing in the space, the loop has to be fast: pick a voice, type, hear it immediately — instant feedback and gratification.

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

What follows is the exact sequence of steps that turns keystrokes into a perfectly composed, AI-enhanced video — ready for the world to judge.

- **Sequence 1 (keystrokes → sound):** keystroke → string → language detection (debounce timer in parallel) → synthesis request → decode response → audio asset.
- **Sequence 2 (editor loop):** audio asset → timeline ↔ editing ↔ pre-composition.
- **Sequence 3 (compose → upload):** compose → transcode → preview → upload.

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
