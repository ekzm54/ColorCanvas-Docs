# ADR-001 — MVVM + Clean Architecture

## Status

Accepted

## Context

ColorCanvas must be maintainable by AI agents over a long period. UI, business logic, data access, rendering, and document storage must remain separate.

## Decision

Use MVVM + Clean Architecture.

## Rationale

- SwiftUI works naturally with ViewModel state.
- Views remain declarative and simple.
- UseCases are testable.
- Repository and Engine protocols support mocks.
- AI agents can understand clear responsibility boundaries.

## Consequences

Positive:
- Strong testability.
- Lower risk of View logic sprawl.
- Easier code review.

Negative:
- More files and protocols.
- Higher initial setup cost.
