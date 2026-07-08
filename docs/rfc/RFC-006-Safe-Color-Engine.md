# RFC-006 — Safe Color Engine

## Status

Ready

## Priority

P0

## Sprint

Sprint-009

## Goal

Implement the core Safe Color system so painting does not affect pixels outside the selected region.

## Scope

- Region Detection
- Region Graph
- Gap Repair
- Region Hit Test
- Region Mask Generation
- Region Mask Cache
- RenderEngine mask clipping integration
- Stroke RegionID support

## Out of Scope

- Brush engine design changes
- Export UI
- Gallery
- Settings
- Document package migration

## Acceptance Criteria

- Closed regions are selectable.
- Nested region hit test chooses the smallest containing region.
- Gaps up to 3px may be repaired.
- Gaps above 3px are not repaired.
- Mask clipping prevents outside-region pixels from changing.
- SafeColorEngine does not import SwiftUI.
- BrushEngine does not know RegionMask.
