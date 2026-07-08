# Sprint 001 — Foundation

## Goal

Create the foundational application runtime structure for ColorCanvas.

## Deliverables

- AppEnvironment
- DependencyContainer skeleton
- AppRouter
- Route
- Base Screen State conventions
- AppError
- ErrorMessageMapper
- Logger skeleton
- Preference skeleton
- Design Token skeleton
- RootView placeholder

## Tasks

1. AppEnvironment
2. DependencyContainer Skeleton
3. AppRouter & Route
4. Base Screen State
5. AppError & ErrorMessageMapper
6. Logger Skeleton
7. Preference Skeleton
8. Design Token Skeleton
9. RootView Placeholder
10. Sprint Verification

## Critical Rules

- AppRouter must not contain business logic.
- View must not create Engines.
- View must not access FileManager.
- State enums are required.
- Preference defaults must be safe.

## Done Criteria

- AppEnvironment exists.
- DependencyContainer skeleton exists.
- AppRouter supports push/pop/popToRoot/modal.
- RootView launches.
- Build/Test/Lint/Format pass.
