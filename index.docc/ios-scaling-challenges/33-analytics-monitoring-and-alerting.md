# Analytics, Monitoring, and Alerting

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Large Mobile Apps")
  @PageImage(purpose: icon, source: "ios-scaling-challenges-33-analytics-monitoring-and-alerting-icon.codex.svg", alt: "Analytics, monitoring, and alerting Icon")
  @PageImage(purpose: card, source: "ios-scaling-challenges-33-analytics-monitoring-and-alerting-card.codex.svg", alt: "Analytics, monitoring, and alerting Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}


@Image(source: "ios-scaling-challenges-33-analytics-monitoring-and-alerting-hero.codex.svg", alt: "Analytics, monitoring, and alerting Hero")

Mobile observability needs client metrics, crash rates, and SLOs.

## Why it Gets Harder at Scale

- Metrics differ across cohorts and app versions.
- Signal loss happens when logging is inconsistent.

## Scale Signals

- No clear crash-free, launch time, or network error budgets.
- Oncall lacks actionable client telemetry.

## Laussat Studio Take

- Standardize metrics and alerting for each release.

## Diagram: Context Snapshot

@Image(source: "ios-scaling-challenges-33-analytics-monitoring-and-alerting-context.mermaid.svg", alt: "Context snapshot")

```mermaid
%% file: ios-scaling-challenges-33-analytics-monitoring-and-alerting-context.svg
%% title: Analytics, monitoring, and alerting - Context snapshot
flowchart LR
  A["Analytics, monitoring, and alerting"] --> B["Constraints and scope"]
  B --> C["Complexity drivers"]
  C --> D["Design tradeoffs"]
  D --> E["Risk: regressions and drift"]
  D --> F["Risk: migration cost"]
  D --> G["Risk: stakeholder misalignment"]
```
