# RFC-001 — Home Screen

## Status

Ready

## Priority

P0

## Sprint

Sprint-004

## Goal

Allow users to continue a recent project or select a new template within 5 seconds after app launch.

## Scope

- Home Header
- Continue Project Card
- Featured Templates
- Categories
- Recent Projects
- Loading / Empty / Error states

## Out of Scope

- Canvas rendering
- Export
- Settings persistence
- Project rename/delete
- Safe Color

## Inputs

- HomeUseCases
- ProjectRepositoryProtocol
- TemplateRepositoryProtocol
- DesignSystem

## Outputs

- HomeView
- HomeViewModel
- HomeState
- Previews
- Tests

## Acceptance Criteria

- Recent project can route to Studio.
- Featured templates are visible.
- Categories route to Gallery.
- Loading, Empty, and Error states are implemented.
- No FileManager or Engine calls from View/ViewModel.
