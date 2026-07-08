# Sprint 012 — Performance & Memory Optimization

## Goal

Measure and optimize Apple Pencil input, Canvas rendering, Safe Color, Gallery/Projects large lists, Auto Save, Export, cache, and memory behavior.

## Related RFC

- RFC-009 — Performance & Memory

## Deliverables

- PerformanceLogger
- Benchmark build configuration
- FrameTimeMonitor
- MemoryMonitor
- Hot Path audit
- Canvas performance tests
- Safe Color performance tests
- Gallery performance checks
- Projects performance checks
- CacheEvictionPolicy
- Auto Save performance audit
- Export performance tests
- Memory warning handling
- Regression gates

## Hot Path

```text
Apple Pencil Input -> StrokeEngine -> BrushEngine -> RenderEngine -> Present
```

## Hot Path Must Not Include

- File IO
- JSON encode/decode
- SVG parsing
- Thumbnail generation
- Export
- Network
- Full canvas render per stroke

## Budgets

- Stroke update: target 2ms.
- Brush dab generation: target 4ms.
- Dirty rect calculation: target 2ms.
- Dirty rect render: target 16ms.
- Safe Color hit test: target 16ms.
- Mask generation: target 300ms.
- Export PNG/PDF: target 5s.
- Total app memory: target 512MB or less.

## Done Criteria

- Performance tests exist.
- Cache eviction never deletes source data.
- Memory warning handling is safe.
- Regression gates report pass/fail.
- Build/Test/Lint/Format pass.
