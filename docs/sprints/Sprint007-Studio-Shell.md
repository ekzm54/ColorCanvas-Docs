# Sprint 007 — Studio Shell Implementation

## Goal

Implement the Studio UI shell before real rendering and Safe Color algorithms are integrated.

## Related RFC

- RFC-004 — Studio Shell

## Deliverables

- StudioState
- StudioViewModel
- StudioView
- CanvasContainer placeholder
- FloatingToolbar
- Command System skeleton
- BottomPalette
- BrushPanel placeholder
- HUD / Toast
- Overlay placeholder
- Preview matrix
- ViewModel/UI tests

## Required State

```swift
enum StudioState {
    case loading
    case preparingMask
    case ready(StudioViewData)
    case drawing(StudioViewData)
    case undoing(StudioViewData)
    case redoing(StudioViewData)
    case saving(StudioViewData)
    case exporting(StudioViewData)
    case error(AppError)
}
```

## Scope

- Studio workspace layout
- Floating toolbar
- Command state skeleton
- Bottom palette
- Brush panel placeholder
- HUD/Toast
- Overlay placeholder
- Export route trigger

## Out of Scope

- Real Canvas rendering
- Metal/CoreGraphics implementation
- Safe Color algorithm
- Real export encoding

## Critical Rules

- CanvasContainer must be replaceable by CanvasEngine later.
- Toolbar actions must route through Command System / ViewModel.
- View must not call RenderEngine or SafeColorEngine directly.
- Canvas must remain the primary visual area.

## Done Criteria

- Studio no longer uses placeholder screen.
- Toolbar and palette exist.
- Export command routes to Export placeholder.
- Build/Test/Lint/Format pass.
