# Book 8 — Engineering Standards & Coding Conventions

## Purpose

Book 8 defines concrete coding standards for AI-generated implementation.

## Required Practices

- Swift 6-ready code.
- Strict concurrency where practical.
- MVVM + Clean Architecture.
- Repository Pattern.
- Command Pattern for toolbar actions.
- Dependency Injection.
- State-driven UI.
- Design Token usage.

## Forbidden

- Force unwrap.
- `try!`.
- Empty `catch`.
- Silent failure.
- `View` accessing `FileManager`.
- `View` calling engines directly.
- `Engine` importing SwiftUI.
- Magic numbers.
- Hard-coded strings in production UI.

## Module Boundary Rule

```text
ColorCanvasUI -> ColorCanvasApplication -> ColorCanvasDomain
ColorCanvasApplication -> Repository Protocols / Engine Protocols
ColorCanvasData -> Document / FileSystem Adapter
ColorCanvasCanvasEngine -> Rendering / Viewport / Stroke
ColorCanvasSafeColor -> Region / Mask / Gap Repair
```

Engines must not depend on UI.
