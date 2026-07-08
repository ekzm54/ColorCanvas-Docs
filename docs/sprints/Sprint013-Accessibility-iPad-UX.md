# Sprint 013 — Accessibility & iPad UX Hardening

## Goal

Improve accessibility and iPad usability across the MVP.

## Related RFC

- RFC-010 — Accessibility & iPad UX

## Deliverables

- Accessibility audit
- VoiceOver labels
- Dynamic Type validation
- Reduce Motion support
- Keyboard navigation
- Pointer support
- Apple Pencil validation
- Orientation validation
- Stage Manager validation
- High Contrast validation
- Accessibility UI tests

## Required Keyboard Shortcuts

- Cmd+Z: Undo
- Shift+Cmd+Z: Redo
- Cmd+E: Export
- Cmd+0: Fit to Screen

## Critical Rules

- Keyboard shortcuts must execute through the Command System.
- Reduce Motion must be respected.
- Color must not be the only state indicator.
- Pointer hover must not change artwork data.
- Apple Pencil remains the highest-priority input.

## Done Criteria

- VoiceOver labels exist for core flows.
- Dynamic Type does not break layouts.
- Keyboard and pointer interactions work.
- iPad orientations are acceptable.
- Build/Test/Lint/Format pass.
