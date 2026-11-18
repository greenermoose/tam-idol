# GNU Coding Standards: README, NEWS, COPYING

Starter note, from the project's published standards
(https://www.gnu.org/prep/standards/), not yet checked line by line.

## What it is

The GNU Project's rules for how a GNU package is laid out and released.
Text documents, under the GNU Free Documentation License. Its "Release
Process" chapter names the files every distribution carries.

## Ideas worth taking

- **A plain-text README at the top, with no extension.** adopt
  (0.1.0). Anyone can read it on any terminal, including a kernel
  console. Every Tamlinux repository already does this.
- **The license in its own file, the notices in another.** adopt
  (0.1.0). GNU keeps the GPL in COPYING; we keep it in LICENSE, with the
  notices (ours and those of code we took) in COPYRIGHT.
- **make, make install, make uninstall, make clean, make check.**
  adopt (0.1.0), with `make test` in place of `make check`, as our
  repositories already have it.

## Things to avoid

- **NEWS and ChangeLog as separate hand-kept histories.** reject. The
  Git history, the work records and ROADMAP.md already say what changed
  and why; a third copy drifts.
- **Autoconf and Automake.** reject. Plain Make is the only build
  system.

## Where to look

"Releases" and "Makefile Conventions" in the GNU Coding Standards.
