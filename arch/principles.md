# Principles of the standard

Why tam-idol's standard is the way it is. A change to the standard
follows these rules, or changes them here first.

## One way of working

Every repository uses the same files and folders, with the same names
and the same README text. Someone who has worked in one repository can
find their way in any other, and an agent starting cold can read
`work/WHATNOW` and carry on.

## Each folder has one job

- `arch/` says how the code is built: true now.
- `ideas/` says what we learned from others: input.
- `plans/` says how we get to the next versions: intent.
- `bugs/` says what is wrong: defects.
- `reviews/` says what someone found when they looked hard: evidence.
- `work/` says what happened in each session and what is next: handoff.

A fact lives in one place. The others point to it.

## The folder explains itself

Each folder has a `README-<folder>` that says what goes in it, how files
are named and what each file holds. The standard part of that text is
the same in every repository; the `IN THIS REPOSITORY` section at the
end is the only part a repository writes for itself. That split lets
`tools/idol-check` compare the standard part exactly.

## Numbered, undated, never reused

Records are named with a letter, a number and a short name: B1, P1, R1,
W1. The number gives the order. The date goes inside the file, because
Git sets every file's date to when it was checked out. A number is never
reused, so a reference to B3 always means the same bug.

## One place for the handoff

`work/WHATNOW` is the one file that says what to do next. Records say
what happened; WHATNOW says where things stand. Every session revises
it as a whole, so it never turns into a history.

## Plain text first

The files people read most (README, each `README-<folder>`, WHATNOW and
the work records) are plain text in 76 columns, readable on a kernel
console without a Markdown renderer. Where Markdown is used, it still
reads well as plain text.

## No paperwork

No index files edited every session, no boilerplate fields, no commits
made only to record their own hash. Records keep what the next reader
needs and cannot get from the diff, including what failed.

## Public by default

The repositories are public. Nothing in them names a session ID, a
transcript, a home-directory path, a private repository or a private
decision number. The private side keeps one line per record mapping it
to its transcript.
