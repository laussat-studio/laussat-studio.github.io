# Diagrams

@Metadata {
  @PageKind(article)
  @PageColor(gray)
  @TitleHeading("Design System Diagrams")
  @PageImage(purpose: icon, source: "system-designs-google-maps-font-system-diagrams-icon.codex.svg", alt: "Diagrams Icon")
  @PageImage(purpose: card, source: "system-designs-google-maps-font-system-diagrams-card.codex.svg", alt: "Diagrams Card")
}

@Options {
  @AutomaticSeeAlso(disabled)
}

@Image(source: "system-designs-google-maps-font-system-diagrams-hero.codex.svg", alt: "Diagrams Hero")

Diagrams now live alongside the narrative sections that explain them. Use this
page as an index and a rendering note, not a gallery.

## Diagram Locations

- Google Maps typography design overview
- Problem context
- Strategy and execution
- Migration details
- Rollout and results
- Search Results example lives in the narrative sections above; no standalone
  diagram required.
- Refactor CLI architecture lives in migration details.

## Source of Truth

Mermaid sources live in `wrkstrm.docc/resources/mermaid/`.
Rendered SVGs live at the bundle root: `wrkstrm.docc/resources/`.

## Diagram: Context Snapshot

## Rendered Exports (Validator Index)

@Image(source: "maps-font-level0.codex.svg", alt: "Google Maps font migration overview")
@Image(source: "maps-font-before-apis.codex.svg", alt: "Before state with five typography APIs")
@Image(source: "maps-font-after-canonical.codex.svg", alt: "After state with canonical tokens and shims")
@Image(source: "maps-font-dependency-map.codex.svg", alt: "Dependency map for shared API first")
@Image(source: "maps-font-decision-tree.codex.svg", alt: "Decision tree for migration strategy")
@Image(source: "maps-font-automation-pipeline.codex.svg", alt: "Automation pipeline")
@Image(source: "maps-font-runtime-flow.codex.svg", alt: "Canonical pipeline runtime flow")
@Image(source: "maps-font-migration-plan.codex.svg", alt: "Migration plan and rollback points")
@Image(source: "maps-font-snapshot-triage.codex.svg", alt: "Snapshot triage loop")
@Image(source: "maps-font-umbrella-before.codex.svg", alt: "Umbrella header coupling before the migration")
@Image(source: "maps-font-umbrella-after.codex.svg", alt: "Compat umbrella during transition")
