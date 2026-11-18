# tam-idol roadmap

tam-idol's version is the version of the standard. A minor version adds
to the standard or changes it; a patch version fixes wording or
`tools/idol-check` without changing what a repository must have.
`plans/P1-standard.md` has the work items.

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
from tam-idol.

## Open points for Fred

- **Branch names.** The standard working branch is dev. libtam, tam,
  tamlinux and tamlinux-tools work on develop, and LIFECYCLE.md names
  develop. Renaming each repository's branch, and the wording in
  LIFECYCLE.md, waits for Fred's word.
- **The tamlinux layout.** tamlinux keeps its code in `commands/` and
  `desktop/`, not `src/`, and has no `tests/` folder at the top. The
  standard either allows that layout or tamlinux moves to it.
- **Blame and provenance.** "Blame" replaces "provenance" as the word
  for which AI did what. Every repository's `AI_PROVENANCE.md` becomes
  `AI-BLAME.md` as it is brought up to standard. tamlinux's
  `docs/ai-provenance-standard.md` and the tools and guides around it
  still say "provenance"; renaming them waits for Fred's word.
- **Existing records.** tam-edit's `reviews/review-001.md` becomes
  `R1-...`; tamlinux's `docs/reviews/` moves to `reviews/`; tamlinux's
  `bugs/0001-...` records become `B1-...`; tam-data's upper-case plan
  names become lower case; `bugs/_template.md` files give way to the
  template in `README-bugs`. Each rename keeps the record's text.
