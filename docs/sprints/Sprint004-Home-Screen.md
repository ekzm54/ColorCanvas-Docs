# Sprint 004 — Home Screen Implementation

## Goal

Implement the Home screen as the main launcher so users can continue a recent project or start from a new template within 5 seconds.

## Related RFC

- RFC-001 — Home Screen

## Deliverables

- HomeState
- HomeViewModel
- HomeView
- ContinueProjectCard
- FeaturedTemplateSection
- CategorySection
- RecentProjectsSection
- Home use case protocols
- Mock Home data
- Preview matrix
- ViewModel tests
- UI tests

## Required State

```swift
enum HomeState {
    case loading
    case ready(HomeViewData)
    case empty
    case error(AppError)
}
```

## Scope

- Header
- Continue Project
- Featured Templates
- Categories
- Recent Projects
- Loading / Empty / Error states

## Out of Scope

- Canvas rendering
- Export
- Project rename/delete
- Settings persistence
- Safe Color

## Critical Rules

- HomeView must not access FileManager.
- HomeViewModel must call UseCases and AppRouter only.
- All UI values must use Design Tokens.
- Search entry may route to Gallery placeholder/search mode.

## Done Criteria

- Home no longer uses placeholder screen.
- Recent project routes to Studio.
- Category routes to Gallery(categoryID).
- Settings button routes to Settings.
- Loading, Empty, Error states implemented.
- Build/Test/Lint/Format pass.
