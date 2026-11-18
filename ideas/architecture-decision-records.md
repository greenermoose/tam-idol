# Architecture decision records

Starter note, from Michael Nygard's 2011 post "Documenting Architecture
Decisions" and the adr.github.io collection, not yet read in full.

## What it is

A convention, not a program: one short numbered file per significant
decision, with its context, the decision and its consequences. Records
are never edited to change a decision; a new record supersedes the old
one.

## Ideas worth taking

- **Numbered records that are never renumbered or reused.** adopt
  (0.1.0). Our B, P, R and W records follow the same rule.
- **A newer record can overrule an older one.** adopt (0.1.0). Our
  plans record Fred's decisions with their date; a later decision
  replaces an earlier one, and the plan says so.
- **Status on every record.** adopt (0.1.0), in bugs/ and plans/.

## Things to avoid

- **A separate decisions folder in every repository.** consider.
  Decisions now live in the plans they shape. A repository with many
  cross-cutting decisions might want one; none does yet.
- **Template fields that get filled with boilerplate.** reject. Our
  records keep only what the next reader needs.

## Where to look

https://adr.github.io/ and the original post linked from it.
