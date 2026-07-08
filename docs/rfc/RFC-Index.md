# RFC Index — ColorCanvas

RFCs define the construction boundary for implementation work. Claude Code and Codex must use RFCs to prevent scope creep.

## Required Workflow

```text
Book -> ADR -> RFC -> Sprint -> Task -> Code -> Review
```

## MVP RFC List

| RFC | Feature | Sprint | Priority | Status |
|---|---|---:|---|---|
| RFC-001 | Home Screen | Sprint-004 | P0 | Ready |
| RFC-002 | Gallery Screen | Sprint-005 | P0 | Planned |
| RFC-003 | Projects Screen | Sprint-006 | P0 | Planned |
| RFC-004 | Studio Shell | Sprint-007 | P0 | Planned |
| RFC-005 | Canvas Engine | Sprint-008 | P0 | Planned |
| RFC-006 | Safe Color Engine | Sprint-009 | P0 | Ready |
| RFC-007 | Export & Finish Experience | Sprint-010 | P0 | Planned |
| RFC-008 | Settings & Preferences | Sprint-011 | P1 | Planned |
| RFC-009 | Performance & Memory | Sprint-012 | P0 | Planned |
| RFC-010 | Accessibility & iPad UX | Sprint-013 | P0 | Planned |
| RFC-011 | QA & Regression | Sprint-014 | P0 | Planned |
| RFC-012 | Release Candidate | Sprint-015 | P0 | Planned |

## RFC Template

```text
# RFC-XXX — Title

## Status

Ready | Planned | Draft | Accepted | Deprecated

## Priority

P0 | P1 | P2 | P3

## Sprint

Sprint-XXX

## Goal

One clear product/engineering goal.

## Scope

What this work may implement.

## Out of Scope

What this work must not implement.

## Inputs

Required dependencies, protocols, repositories, documents, or engines.

## Outputs

Expected files/modules/features.

## Acceptance Criteria

Concrete pass/fail criteria.

## Tests Required

Required test types.

## Performance Budget

Budgets if relevant.

## Accessibility Requirements

Accessibility requirements if UI is involved.

## Related ADR

Architecture decisions that apply.
```
