# Sprint 009 — Safe Color Engine Implementation

## Goal

Implement the core Safe Color system so users can color inside a selected region without paint bleeding outside the line art.

## Deliverables

- Safe Color core models
- SVG path model skeleton
- RegionGraphBuilder
- SmartGapRepair
- RegionAnalyzer
- RegionHitTester
- RegionMaskGenerator
- RegionMaskCache
- SafeColorEngine
- RenderEngine mask clipping integration
- Stroke RegionID integration
- Studio Safe Color UI integration
- Error recovery
- Safe Color tests

## Critical Rules

- SafeColorEngine must not import SwiftUI.
- SafeColorEngine must not render pixels.
- BrushEngine must not know RegionMask.
- RenderEngine applies mask clipping.
- RegionID must be stable.
- Gap repair threshold is 3px maximum.
- Cache deletion must not affect source data.

## Done Criteria

- Mask clipping prevents outside-region pixel changes.
- Region hit testing handles nested regions.
- Gap Repair behavior is tested.
- Safe Color errors do not crash the app.
- Build/Test/Lint/Format pass.
