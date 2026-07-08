# Claude Code Guide

Claude Code is the primary implementation agent for ColorCanvas.

## Startup Checklist

Before implementing anything, read:

1. `AI_RULES.md`
2. Relevant Book files in `docs/books/`
3. Relevant ADR files in `docs/adr/`
4. Relevant RFC files in `docs/rfc/`
5. Active Sprint file in `docs/sprints/`

## Implementation Rule

Implement only the active Sprint and only the active RFC scope.

## Required Output

When completing a task, report:

1. Goal
2. Files changed
3. Architecture notes
4. Tests added
5. Build/Test/Lint result
6. Remaining risks

## Forbidden

- Broad refactoring without explicit task scope
- New features not in the RFC
- Placeholder TODOs without issue ID
- Hard-coded UI values
- Business logic in Views
