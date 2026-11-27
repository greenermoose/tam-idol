# The ROADMAP.md standard

Every Tamlinux repository keeps a `ROADMAP.md` at its root so that anyone
opening the repository can see at a glance where the program stands, how
far it has progressed, what its phases and milestones are, and which plan
covers each phase.

## Required structure

A standard `ROADMAP.md` has these sections in order:

1. **Title and summary.** `# <repo> roadmap`, a one-sentence description
   of the project, and a short metadata list:
   - `- **Current version:**` the current version from `VERSION` (and
     branch, e.g. `dev`; dual-version repositories list both).
   - `- **Progress:**` how many phases are done and what is next.
   - `- **Versioning:**` how version numbers map to phases and milestones.
2. **`## Phase summary`.** A Markdown table with one row per phase:
   `Phase | Versions | Goal | Plan | Status`. Every phase links directly
   to its `plans/P<n>-<name>.md` file.
3. **`## Decided`** *(optional).* Settled design decisions with their
   dates, kept concise. Include only when the repository has recorded
   decisions.
4. **`## Phases and milestones`.** One subsection per phase:
   `### Phase P<n>: <Title> (<versions>) — [P<n>-<name>.md](plans/P<n>-<name>.md)`
   followed by a `Version | Milestone | Status` table listing each
   milestone in that phase. Every milestone appears once, under its phase.
5. **`## How a milestone is done`.** The completion rule: acceptance
   checks in the phase plan pass, Fred tries the build, and `VERSION`,
   the phase plan, and `ROADMAP.md` update in the same change.

## Status values

Use these status values in both the phase summary and milestone tables:

- `Done (YYYY-MM-DD)` — completed on that date (`Done` if historical date
  is unknown).
- `In progress` — active work on branch `dev`.
- `Planned` — scoped for a future phase or milestone.
- `Deferred` — parked until Fred chooses to start it.

## Relation to plans

Every milestone belongs to a phase, and every phase has a plan file in
`plans/P<n>-<name>.md` (following `plans/README-plans`). `ROADMAP.md`
gives the at-a-glance overview; detailed work items, acceptance checks,
dependencies, risks, and open points live in the phase plan.

## Keeping ROADMAP.md current

When a milestone lands:

1. Bump `VERSION` in the same commit (for code changes).
2. Update the phase plan's status line.
3. Update `ROADMAP.md`: the `Current version` and `Progress` lines, the
   milestone's `Status` cell, and the phase's `Status` cell when the
   phase finishes.

## What `tools/idol-check` verifies

- `ROADMAP.md` exists and contains `- **Current version:**`,
  `## Phase summary`, `## Phases and milestones`, and
  `## How a milestone is done`.
- At least one `### Phase P<n>:` heading is present, and every
  `### Phase P<n>:` heading links to a `plans/P<n>-<name>.md` file.
- Every `plans/P<n>-<name>.md` file linked from `ROADMAP.md` exists on
  disk.
