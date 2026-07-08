# ADR-002 — Repository Pattern

## Status

Accepted

## Context

UI and ViewModels must not access storage, file system, document packages, or caches directly.

## Decision

Use Repository Pattern with protocol-based dependencies.

## Rationale

- Testable with mock repositories.
- Allows local storage now and cloud/sync later.
- Prevents UI from depending on implementation details.
- Keeps Document Engine and FileSystem Adapter behind stable interfaces.

## Consequences

- More protocol definitions.
- Requires clear dependency injection.
