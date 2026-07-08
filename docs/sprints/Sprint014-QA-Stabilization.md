# Sprint 014 — QA, Regression & Stabilization

## Goal

Run full MVP QA, regression, recovery, document corruption, export, Safe Color, accessibility, and performance smoke validation.

## Related RFC

- RFC-011 — QA & Regression

## Deliverables

- Full regression test plan
- End-to-end flow tests
- Crash recovery tests
- Document corruption tests
- Safe Color accuracy QA
- Export validation QA
- Performance smoke tests
- Accessibility regression tests
- QA bug list
- Release blocker list
- Final QA report

## P0 Examples

- Data loss
- Crash on launch
- Export corrupts project
- Safe Color paints outside selected region
- App cannot open existing project

## Critical Rules

- No new features during stabilization.
- Fix only P0 and P1 issues unless explicitly approved.
- Every fix must include a regression test.
- Project source data must remain protected.

## Done Criteria

- Full regression suite completed.
- P0/P1 blockers resolved.
- Final QA report exists.
- Release readiness verdict is available.
- Build/Test/Lint/Format pass.
