# Device and OS Fragmentation

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-11-device-and-os-fragmentation-icon.codex.svg", alt: "Device and OS fragmentation Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-11-device-and-os-fragmentation-card.codex.svg", alt: "Device and OS fragmentation Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-11-device-and-os-fragmentation-hero.codex.svg", alt: "Device and OS fragmentation Hero")

iOS fragmentation is subtle: iPad multitasking, input modes, and hardware
capability tiers.

## Why it Gets Harder at Scale

- Layouts must survive split view, rotation, and pointer input.
- Performance profiles vary across memory and GPU classes.

## Scale Signals

- iPad-specific bugs rise after major releases.
- Features behave differently on older devices.

## Laussat Studio Take

- Build capability-driven UI paths and test real device tiers.

## Diagram: Context Snapshot

@Image(source: "ios-scaling-challenges-11-device-and-os-fragmentation-context.mermaid.svg", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-11-device-and-os-fragmentation-context.svg
%% title: Device and OS fragmentation - Context snapshot
flowchart LR
  A["Device and OS fragmentation"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
