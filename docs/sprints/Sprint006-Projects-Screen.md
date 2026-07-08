# Sprint 006 — Projects Screen Implementation

## Goal

Implement the Projects screen so users can find, open, rename, duplicate, delete, favorite, and manage saved artwork safely.

## Related RFC

- RFC-003 — Projects Screen

## Deliverables

- ProjectsState
- ProjectsViewModel
- ProjectsView
- ProjectGrid
- ProjectCard expansion
- ProjectContextMenu
- RenameProjectSheet
- DeleteProjectDialog
- Mock ProjectRepository
- Preview matrix
- ViewModel/UI tests

## Required State

```swift
enum ProjectsState {
    case loading
    case ready(ProjectsViewData)
    case empty
    case deleting(projectID: ProjectID)
    case renaming(projectID: ProjectID)
    case error(AppError)
}
```

## Scope

- Project list
- Search
- Filter
- Sort
- Open project
- Rename
- Duplicate
- Favorite
- Delete confirmation

## Out of Scope

- Canvas rendering
- Safe Color
- Export Engine
- Project document migration

## Critical Rules

- Delete must require confirmation.
- Clear distinction between cache deletion and project deletion.
- ProjectRepository mock must not access real file system.
- Project cards must include accessible labels.

## Done Criteria

- Projects no longer uses placeholder screen.
- Search/filter/sort work with mock data.
- Rename validation prevents empty title.
- Delete requires confirmation.
- Build/Test/Lint/Format pass.
