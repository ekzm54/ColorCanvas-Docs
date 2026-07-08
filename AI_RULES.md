# AI Rules

These rules apply to all AI agents working on ColorCanvas.

## Priority

```text
Book 0 -> ADR -> RFC -> Sprint -> Task -> Code
```

## Non-Negotiable Rules

1. Do not exceed the active RFC scope.
2. Do not implement features outside the active Sprint.
3. Do not hard-code UI colors, spacing, typography, radius, or animation values.
4. Do not put business logic in SwiftUI Views.
5. Do not let UI directly access FileManager, RenderEngine, SafeColorEngine, or DocumentEngine.
6. Always use State enums instead of multiple boolean flags.
7. Always add tests for new behavior.
8. Protect user artwork above all else.
9. Never remove Undo, Auto Save, Recovery, or Safe Color to solve performance problems.
10. Run build, test, lint, and format before marking work complete.
