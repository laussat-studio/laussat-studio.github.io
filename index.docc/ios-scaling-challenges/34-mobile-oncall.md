# Mobile Oncall

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-34-mobile-oncall-icon.codex.svg", alt: "Mobile oncall Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-34-mobile-oncall-card.codex.svg", alt: "Mobile oncall Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-34-mobile-oncall-hero.codex.svg", alt: "Mobile oncall Hero")

Mobile incidents require quick triage, rollback paths, and server gating.

## Why it Gets Harder at Scale

- Rollout timelines and App Store delays slow mitigation.
- Cross-platform coordination complicates incident response.

## Scale Signals

- Oncall lacks clear runbooks for client regressions.
- Incidents repeat without postmortem follow-through.

## Laussat Studio Take

- Maintain incident playbooks and rehearsal drills.

## Diagram: Context Snapshot

@Image(source: "ios-scaling-challenges-34-mobile-oncall-context.mermaid.svg", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-34-mobile-oncall-context.svg
%% title: Mobile oncall - Context snapshot
flowchart LR
  A["Mobile oncall"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
