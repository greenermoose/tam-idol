# P3: Standard ROADMAP.md format and rollout

- **Status:** done (version 1.3.0, 2026-11-26)
- **Versions:** 1.3.0

## Goal

Standardize `ROADMAP.md` across every `tam-idol`-governed repository so
anyone can see at a glance a program's current version, progress across
phases, per-phase milestone status tables, and links to `plans/P<n>-*.md`
for every milestone.

## Versions

- **1.3.0:**
  - Define the `ROADMAP.md` standard in `arch/roadmap.md`, update
    `arch/layout.md` and `README`, and convert `tam-idol/ROADMAP.md` to
    be the live exemplar.
  - Extend `tools/idol-check` to verify the required `ROADMAP.md`
    sections and that every phase links to an existing
    `plans/P<n>-<name>.md` file.
  - Roll out the standard across all 16 other `tam-idol` repositories,
    creating missing `plans/P<n>-<name>.md` files so every milestone is
    associated with a plan.

## Acceptance

- `tools/idol-check` exits 0 on `tam-idol` and passes all `ROADMAP.md`
  and plan-link checks on every `tam-idol` repository.
- Every `ROADMAP.md` has accurate current versions, phase summary table,
  per-phase milestone tables, and valid plan links.

## Dependencies

None (`tools/idol-check` stays POSIX `sh` with `grep`, `sed`, `sort`,
`cmp`, and `git`).

## Risks

- **Stale version numbers or missing plans.** Reconcile each repository's
  `ROADMAP.md` against its `VERSION` and recent `git log`; never reuse
  existing `P<n>` numbers.
- **Breaking existing links in `tam`.** Keep `tam/docs/plans/` intact and
  verify with `tam/tools/check-repo.py`.

## Open points

None.
