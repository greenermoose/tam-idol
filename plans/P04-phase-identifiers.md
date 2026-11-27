# P04 · Separate phase and plan identifiers

**Phase:** PH04

**Status:** In progress for 1.4.0.

## Goal

Give roadmap phases chronological PHxx identifiers and keep independent,
stable Pxx identifiers for plans, including supporting work.

## Milestone and acceptance

Document both identifiers and adopt them in tam-idol and tamlinux.
The checker accepts both updated repositories and an unchanged 1.3.0
repository. It detects malformed phase headings and missing plan links.
Legacy repositories can adopt the new layout individually.

The checker continues to use POSIX shell and the existing command-line tools.
The prior plans README text remains available for legacy checks.
