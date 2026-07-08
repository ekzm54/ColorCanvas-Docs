# Sprint 005 — Gallery Screen Implementation

## Goal

Implement Gallery as the template discovery hub where users can search, filter, preview, and select coloring templates.

## Related RFC

- RFC-002 — Gallery Screen

## Deliverables

- GalleryState
- GalleryViewModel
- GalleryView
- GallerySearchBar
- CategoryChipRow
- FeaturedTemplateCarousel
- TemplateGrid
- TemplateDetailSheet
- Mock TemplateRepository
- Preview matrix
- ViewModel/UI tests

## Required State

```swift
enum GalleryState {
    case loading
    case browsing(GalleryViewData)
    case searching(query: String, results: [GalleryTemplateSummary])
    case empty
    case error(AppError)
}
```

## Scope

- Search
- Category filtering
- Featured templates
- Template grid
- Template detail bottom sheet
- Favorite placeholder
- Start project placeholder/flow hook

## Out of Scope

- Real canvas rendering
- Brush system
- Export
- Settings
- Safe Color

## Critical Rules

- GalleryViewModel must not access FileManager.
- TemplateRepository mock must be deterministic.
- TemplateGrid must use lazy layout.
- TemplateDetailSheet must not create documents directly in View.

## Done Criteria

- Gallery no longer uses placeholder screen.
- Search and category filtering work with mock templates.
- Template detail sheet appears.
- Build/Test/Lint/Format pass.
