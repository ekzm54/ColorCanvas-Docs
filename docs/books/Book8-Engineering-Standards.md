# Book 8 — Engineering Standards & Coding Conventions

## Purpose

Book 8 defines concrete coding standards for AI-generated Android implementation.

## Required Practices

- Kotlin with Gradle Kotlin DSL.
- Jetpack Compose and Material 3.
- Coroutines and Flow for asynchronous state.
- Android ViewModel.
- MVVM + Clean Architecture.
- Repository Pattern.
- Command or event pattern for toolbar actions.
- Dependency Injection.
- State-driven UI.
- Design Token usage.
- Offline-first persistence.

## Forbidden

- Business logic inside composables.
- Composables accessing files, databases, repositories, or engines directly.
- Core engines depending on Compose UI.
- Silent failure.
- Empty exception handling.
- Hard-coded design values outside token definitions.
- Hard-coded production strings outside resources.
- Blocking IO on the main thread.
- iOS, SwiftUI, UIKit, CoreGraphics, or Metal-specific code.

## Module Boundary Rule

```text
:app -> :feature:* -> :core:domain
:feature:* -> :core:designsystem / :core:ui / :core:common
:core:data -> :core:domain
:core:canvas -> rendering / viewport / stroke
:core:safecolor -> region / mask / gap repair
:core:document -> project package and persistence
:core:export -> PNG / PDF / sharing payload
```

## UI State Rule

- Screen state must be represented with immutable data classes and sealed interfaces/classes where appropriate.
- Composables receive state and callbacks.
- One-shot effects must use an explicit effect/event channel.

## Testing Rule

- Unit tests for ViewModels, UseCases, repositories, and engines.
- Compose UI tests for user flows.
- Instrumented tests only where Android framework behavior is required.
- Rendering and Safe Color core logic should remain JVM-testable where practical.

Engines must not depend on UI.
