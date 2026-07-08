# Sprint Index — ColorCanvas MVP

This index defines the complete MVP sprint sequence.

## Sprint Flow

```text
Sprint 000 -> Sprint 001 -> Sprint 002 -> Sprint 003 -> Sprint 004 -> Sprint 005 -> Sprint 006 -> Sprint 007 -> Sprint 008 -> Sprint 009 -> Sprint 010 -> Sprint 011 -> Sprint 012 -> Sprint 013 -> Sprint 014 -> Sprint 015
```

## MVP Sprint List

| Sprint | Name | Goal |
|---:|---|---|
| 000 | Project Bootstrap | Create monorepo, package placeholders, scripts, CI, initial docs. |
| 001 | Foundation | AppEnvironment, DependencyContainer, AppRouter, base state, errors, logger, preferences. |
| 002 | Design System | Tokens, colors, typography, state tokens, buttons, cards, preview matrix. |
| 003 | Navigation & App Shell | Route, ModalRoute, NavigationStack, placeholder screens, deep link skeleton. |
| 004 | Home Screen | App launcher with recent projects, featured templates, categories. |
| 005 | Gallery Screen | Template search, category filters, template detail sheet. |
| 006 | Projects Screen | Project list, search, filter, rename, duplicate, delete. |
| 007 | Studio Shell | Canvas shell, toolbar, palette, HUD, overlay placeholders. |
| 008 | Canvas Engine | Viewport, coordinate transform, stroke, brush, dirty rect, CoreGraphics fallback. |
| 009 | Safe Color Engine | Region, mask, gap repair, hit test, clipping, cache. |
| 010 | Export & Finish | PNG/PDF export, share sheet, finish screen. |
| 011 | Settings & Preferences | Appearance, Apple Pencil, Safe Color, Export, Accessibility, Storage settings. |
| 012 | Performance & Memory | Performance logger, benchmarks, frame/memory monitor, cache eviction. |
| 013 | Accessibility & iPad UX | VoiceOver, Dynamic Type, Reduce Motion, keyboard, pointer, iPad layout hardening. |
| 014 | QA & Stabilization | Regression, recovery, corruption tests, safe color accuracy, export validation. |
| 015 | Release Candidate | Versioning, privacy, App Store assets, crash monitoring, release checklist. |

## Sprint Execution Rule

Claude Code must implement only the active Sprint. Codex must review against the active RFC and Sprint.

## Sprint Done Criteria

```text
Build PASS
Tests PASS
Lint PASS
Format PASS
Architecture review PASS
Accessibility review PASS if UI
Performance review PASS if hot path or rendering
```
