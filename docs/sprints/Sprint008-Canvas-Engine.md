# Sprint 008 — Canvas Engine Implementation

## Goal

Implement the Canvas Engine foundation: coordinates, viewport, stroke input, basic brush, dirty rects, render surfaces, CoreGraphics fallback, and integration with Studio CanvasContainer.

## Related RFC

- RFC-005 — Canvas Engine

## Deliverables

- Canvas core models
- CoordinateTransformer
- CanvasViewport logic
- CanvasSession
- Stroke input models
- Basic RoundBrushEngine
- StrokeEngine skeleton
- DirtyRectCalculator
- RenderSurface models
- CoreGraphicsRenderEngine fallback
- MetalRenderEngine skeleton
- CanvasViewAdapter
- Canvas Engine tests

## Scope

- Canvas Space coordinate system
- Viewport zoom/pan
- Stroke begin/update/end
- BrushDab generation
- Dirty Rect calculation
- Basic rendering fallback
- Studio CanvasContainer integration

## Out of Scope

- Safe Color Region/Mask
- PNG/PDF export
- Document save format
- Gallery/Projects UI

## Critical Rules

- Stroke data must store Canvas Space coordinates only.
- CanvasEngine core models must not import SwiftUI.
- BrushEngine outputs BrushDabs only; it must not render pixels.
- RenderEngine renders pixels.
- Dirty Rect must be used for stroke rendering.
- CoreGraphics fallback must work before Metal acceleration.

## Performance Budget

- Coordinate transform: deterministic and testable.
- Dirty rect calculation: target 2ms.
- Stroke update: target 2ms.
- Brush dab generation: target 4ms.
- Dirty rect render: target 16ms.

## Done Criteria

- Studio CanvasContainer connected to CanvasEngine.
- Basic strokes render through CoreGraphics fallback.
- Metal skeleton exists but does not block build.
- Tests cover coordinate conversion, viewport, stroke, brush, dirty rect, layer order.
- Build/Test/Lint/Format pass.
