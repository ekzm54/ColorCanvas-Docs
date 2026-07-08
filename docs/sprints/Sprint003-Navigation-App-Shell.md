# Sprint 003 — Navigation & App Shell

## Goal

Connect AppRouter, NavigationStack, Route, ModalRoute, and placeholder screens into a stable app shell.

## Deliverables

- Route
- ModalRoute
- AppRouter
- RootView NavigationStack
- Placeholder screens
- PlaceholderScreen component
- DeepLinkRouter skeleton
- Navigation tests
- Navigation previews

## Routes

- home
- gallery(categoryID?)
- projects
- settings
- studio(projectID)
- export(projectID)

## Modal Routes

- templateDetail(templateID)
- colorPicker
- brushPanel
- renameProject(projectID)
- deleteConfirmation(projectID)
- shareSheet(exportID)

## Critical Rules

- Route must not contain View.
- AppRouter must not call UseCases.
- AppRouter must not access Repository.
- Modal navigation must be separate from push navigation.

## Done Criteria

- App launches to RootView.
- Home placeholder navigates to Gallery/Projects/Settings.
- Gallery/Projects can navigate to Studio placeholder.
- Studio can navigate to Export placeholder.
- Navigation tests pass.
