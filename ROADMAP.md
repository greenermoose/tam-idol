# tam-idol roadmap

tam-idol's version is the version of the standard. A minor version adds
to the standard or changes it; a patch version fixes wording or
`tools/idol-check` without changing what a repository must have.
`plans/P1-standard.md` has the work items.

## 0.2.1: allow `work/ai-blame-standard.md`

Patch update to `tools/idol-check` and `arch/layout.md` so `tamlinux`
can host the public AI blame standard at `work/ai-blame-standard.md`
(work-session paperwork rather than code architecture). No other
repository needs to change. Done 2026-11-20 (W14).

## 0.2.0: work history lives under work/

There is no `docs/ai/` folder. Records from before the 2026-11-17
cutover live in `work/history/`, read-only and not indexed; new
sessions write `work/W<n>-<name>`. `tools/idol-check` reports a
`docs/ai/` directory as a gap. Done 2026-11-20 under D278;
repositories following the standard update their README and
`work/README-work` with the rollout.

## 0.1.0: the standard is written down

The standard set, the `README-<folder>` text for arch, bugs, ideas,
plans, reviews and work, the procedures in `README`, and
`tools/idol-check`. tam-mail is the first repository to follow it,
which tests the standard on a real project. Done 2026-11-18.

## Before 1.0.0: every other repository, one at a time

Bringing a repository up to standard does not change tam-idol's
version; changing the standard on the way does. Each repository passes
`tools/idol-check`, in this order: the newest and closest to the
standard first.

1. tam-clam
2. tam-pane
3. tam-last
4. tam-data
5. tam-ring
6. tam-file
7. tam-edit
8. libtam
9. tam
10. tamlinux-tools
11. tamlinux

What every repository still needs, as of 2026-11-18:

- `AI-BLAME.md` in place of `AI_PROVENANCE.md`;
- the "Follows the tam-idol ... standard" line in README;
- an `IN THIS REPOSITORY` section in every `README-<folder>`, with the
  text above it made the same as tam-idol's;
- `reviews/README-reviews`.

Beyond those, `tools/idol-check <repository>` gives the full list.

## 1.0.0: every repository follows the standard

Every repository passes `tools/idol-check`, and a new repository starts
from tam-idol. Done and tagged 2026-11-20 (W14).

## Done since 0.1.0

- **Branch names (D272).** `develop` was renamed to `dev` in libtam,
  tam, tamlinux, tamlinux-packages and tamlinux-tools on 2026-11-20.
  LIFECYCLE.md, agent routing, candidate preparation, tools and tests
  name `dev`; `test` and `main` kept their names and rules. The version
  of the standard did not change.
- **The tamlinux layout.** Re-examined, reorganized into `src/`,
  `tests/`, `arch/`, `bugs/`, `ideas/`, `plans/`, `reviews/`, and
  `work/`, and brought up to the `tam-idol` 0.2.1 standard on branch
  `dev` (W14, 2026-11-20).
- **Blame, everywhere.** Renamed every remaining `AI_PROVENANCE.md` to
  `AI-BLAME.md` (including the 8 in-repo `fred.*` plugins), moved the
  public standard to `tamlinux/work/ai-blame-standard.md`, renamed the
  `ai-blame` skill, guides, routing, memories, and private `blame/`
  ledger, and repointed `AI-BLAME.md` links across all free repos
  (`tam/AI-BLAME.md` queued for Codex while its exclusive claim holds).
  Dated historical records were left untouched (W14, 2026-11-20).

## Still to settle

- **Existing records.** tam-edit's `reviews/review-001.md` becomes
  `R1-...`; tamlinux's `docs/reviews/` moves to `reviews/`; tamlinux's
  `bugs/0001-...` records become `B1-...`; tam-data's upper-case plan
  names become lower case; `bugs/_template.md` files give way to the
  template in `README-bugs`. Each rename keeps the record's text.
