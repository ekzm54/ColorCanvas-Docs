# Sprint 010 — Export & Finish Experience Implementation

## Goal

Implement PNG/PDF export, Share Sheet integration, and the final completion experience.

## Related RFC

- RFC-007 — Export & Finish Experience

## Deliverables

- ExportState
- ExportViewModel
- ExportView
- Export core models
- ExportEngineProtocol
- PNGExportRenderer
- PDFExportRenderer
- ExportRepository
- Export use cases
- ShareSheetAdapter
- FinishScreen
- Export tests

## Scope

- Prepare export
- PNG export
- PDF export
- Quality selection
- File name editing
- Progress state
- Share Sheet
- Finish screen

## Out of Scope

- Canvas rendering engine implementation
- Settings screen
- Gallery
- Safe Color algorithm

## Critical Rules

- Export must not mutate project source data.
- Export output must exclude overlays, HUD, toast, brush cursor, and selection highlight.
- ExportEngine must not present UI.
- ShareSheetAdapter belongs to platform UI layer.
- Duplicate export must be disabled while exporting.

## Performance Budget

- PNG export: target 5 seconds or less.
- PDF export: target 5 seconds or less.
- Share Sheet display: target 500ms or less.

## Done Criteria

- PNG/PDF export works from Studio export command.
- Export failures are recoverable.
- Finish screen appears after success.
- Build/Test/Lint/Format pass.
