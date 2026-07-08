# AI Agent Workflow

## Roles

- Claude Code: implementation
- Codex: review and correction recommendations
- Testing Agent: test coverage and regression validation
- Performance Agent: performance budget verification
- Release Agent: release checklist and operations validation

## Standard Workflow

```text
RFC selected
↓
Sprint selected
↓
Claude Code implements
↓
Build/Test/Lint
↓
Codex reviews
↓
Claude Code fixes
↓
Testing Agent validates
↓
Merge
```

## Review Rule

Codex should suggest targeted fixes only. It must not rewrite the whole implementation unless the active task explicitly requests refactoring.
