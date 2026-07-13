# Android Migration Plan

## Decision

ColorCanvas is now an Android-first application.

## Target Stack

- Kotlin
- Jetpack Compose
- Material 3
- Coroutines and Flow
- Android ViewModel
- Gradle Kotlin DSL
- Hilt or constructor-based dependency injection
- Room and document-based local persistence as appropriate
- Android Canvas / graphics APIs behind engine interfaces

## Migration Principle

Preserve product requirements, domain concepts, Safe Color behavior, document safety rules, and Sprint intent. Replace iOS-specific implementation details with Android equivalents.

## Platform Mapping

| Previous iOS concept | Android replacement |
|---|---|
| Swift | Kotlin |
| SwiftUI | Jetpack Compose |
| ObservableObject | Android ViewModel + StateFlow |
| NavigationStack | Navigation Compose |
| UserDefaults | DataStore |
| FileManager | java.nio / Android storage adapter |
| CoreGraphics | Android Canvas / Bitmap APIs |
| Metal | OpenGL ES, Vulkan, RenderEffect, or optimized Canvas path when justified |
| Apple Pencil | Android stylus input, MotionEvent pressure/tilt/tool type |
| Share Sheet | Android Sharesheet via Intent |
| Xcode tests | JUnit, Compose UI tests, instrumented tests |

## Repository Strategy

Do not erase history. Create an Android replatform branch from the current main branch.

Recommended branch:

```text
replatform/android
```

The current Swift implementation may be retained temporarily under an archive folder or removed in the Android migration PR after review.

## Android Module Plan

```text
:app
:feature:home
:feature:gallery
:feature:projects
:feature:studio
:feature:export
:feature:settings
:core:domain
:core:data
:core:common
:core:ui
:core:designsystem
:core:canvas
:core:safecolor
:core:document
:core:export
:core:testing
```

## Sprint Mapping

Sprint numbers remain unchanged.

- Sprint 000 becomes Android Gradle multi-module bootstrap.
- Sprint 001 becomes Android foundation, DI, navigation contracts, error handling, and DataStore skeleton.
- Sprint 002 becomes Compose Material 3 design system.
- Sprint 003 becomes Navigation Compose app shell.
- Sprint 004–007 become Compose feature screens.
- Sprint 008 becomes Android Canvas/stylus engine.
- Sprint 009 remains Safe Color Engine with Android bitmap/mask integration.
- Sprint 010 uses Android image/PDF export and Sharesheet.
- Sprint 011 uses DataStore preferences.
- Sprint 012–015 use Android performance, accessibility, QA, and Play Store release requirements.

## Immediate Actions

1. Stop adding Swift or SwiftUI implementation.
2. Create `replatform/android` branch.
3. Inventory current code and preserve reusable product/domain documentation.
4. Replace iOS project structure with Android Gradle multi-module structure.
5. Update Sprints and RFCs with Android terminology.
6. Restart implementation from Android Sprint 000.

## Safety Rules

- Do not force-push over existing history.
- Do not delete current implementation until the Android branch builds.
- Do not mix Swift and Kotlin architecture in active modules.
- Preserve user artwork safety, Auto Save, recovery, and Safe Color requirements.
