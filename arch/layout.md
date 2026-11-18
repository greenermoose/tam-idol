# The standard layout

This is the set `tools/idol-check` checks. The script keeps its own copy
of these lists; change both in the same commit.

## Required in every repository

    README              plain text; ends WHERE THINGS ARE; names the
                        tam-idol version it follows
    COPYRIGHT           our notice, and the notices of code we took
    LICENSE             GNU GPL version 3, unchanged
    VERSION             one line, the current version
    ROADMAP.md          milestones with version numbers
    UPSTREAM.md         code taken from other projects
    AI-BLAME.md         how AI work is recorded
    .gitignore          build output

    arch/README-arch
    bugs/README-bugs
    ideas/README-ideas
    plans/README-plans
    reviews/README-reviews
    work/README-work
    work/WHATNOW

## Required where the repository keeps reference clones

    ideas/sources            one clone per line
    tools/pull-references    clones or updates them

## Required in a repository with code

    Makefile        targets: all (the default), test, install,
                    uninstall, clean; PREFIX defaults to $HOME/.local
    src/            the source
    tests/          what make test runs

`include/` and `tools/` are added when the project needs them.

## Records

    bugs/B<n>-<name>.md      one bug
    plans/P<n>-<name>.md     one work phase
    reviews/R<n>-<name>.md   one review
    work/W<n>-<name>         one work session (plain text)

## Branches

    dev     where work happens; agents push it freely
    main    moves only on Fred's word, as do tags and releases

## The README-<folder> rule

Everything above the line `IN THIS REPOSITORY` in a repository's
`README-<folder>` is the same as in tam-idol, word for word.
The section from that line on is the repository's own.
