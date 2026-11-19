# P1: the standard, and every repository following it

- **Status:** in progress, 0.1.0 (2026-11-18)
- **Versions:** 0.1.0 to 1.0.0

## Goal

Every Tamlinux repository has the same files and folders, with the same
`README-<folder>` text, and follows the same procedures, so that a
person or an agent who knows one repository can work in any of them.

## Versions

**0.1.0, the standard written down.** README with the standard set and
the procedures; `arch/principles.md` and `arch/layout.md`; the six
`README-<folder>` files written about "this repository", with an
`IN THIS REPOSITORY` section at the end of each; `tools/idol-check`;
`tools/pull-references`. tam-mail, the first repository to follow it,
gets everything it is missing, and its folder READMEs are made standard
with its own notes moved into `IN THIS REPOSITORY`. Done 2026-11-18.

**0.1.x and later, the other repositories.** One repository per step,
in the order ROADMAP.md gives. A step that changes the standard bumps
tam-idol's version; one that only applies it does not. For each:

1. Run `tools/idol-check <repository>`.
2. Rename `AI_PROVENANCE.md` to `AI-BLAME.md` and reword it.
3. Make each `README-<folder>` standard, moving the repository's own
   text into `IN THIS REPOSITORY`.
4. Add what is missing (reviews/, VERSION, UPSTREAM.md, ...).
5. Rename records that break the naming rule, keeping their text.
6. Add the "Follows the tam-idol ... standard" line to README.
7. Write the repository's W record and revise its WHATNOW.

A repository's step is one W record and one commit in that repository,
plus a line here when it is done.

**1.0.0.** `tools/idol-check` passes for every repository.

## Acceptance

`tools/idol-check <repository>` exits 0, and the repository's WHATNOW
says what was changed.

## Dependencies

None. `tools/idol-check` and `tools/pull-references` are POSIX sh with
git, grep, sed and cmp.

## Risks

- **A README rewrite loses a repository's own notes.** Move them into
  `IN THIS REPOSITORY`; never delete them.
- **Renaming a record breaks links to it.** grep the repository for the
  old name and fix every link in the same commit.
- **A shared checkout.** Other sessions may be working in the same
  repository; claim only the paths being changed.

## Open points

Fred decided three on 2026-11-18: `develop` becomes `dev` everywhere;
tamlinux is re-examined, cleaned up and reorganized to the standard;
"blame" replaces "provenance" everywhere. ROADMAP.md has the detail and
what is still to settle. Each is separate work, not a step of this plan,
but a repository brought up to standard after its part is done needs no
further change for it.

## Done

- tam-mail: 2026-11-18 (tam-idol 0.1.0).
- tam-file: 2026-11-18 (tam-idol 0.1.0).
- tam-clam: 2026-11-18 (tam-idol 0.1.0).
