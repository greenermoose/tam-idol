# tam-idol roadmap

`tam-idol` is the exemplar Tamlinux repository defining the standard
layout, folder READMEs, keybinding rules, roadmap format, and
`tools/idol-check`.

- **Current version:** `1.4.0` (branch `dev`)
- **Progress:** 3 of 4 phases done. PH04 adds separate phase and plan IDs.
- **Versioning:** `VERSION` is the version of the standard; minor adds to
  or changes the standard, patch fixes wording or `tools/idol-check`
  without changing what a repository must have.

## Phase summary

| Phase | Versions | Goal | Plan | Status |
| --- | --- | --- | --- | --- |
| **PH01** | 0.1.0–1.0.0 | Write down the standard and bring every Tamlinux repository up to it | [P01-standard.md](plans/P01-standard.md) | Done (2026-11-20) |
| **PH02** | 1.1.0–1.2.1 | Add optional `sandbox/` folder and shared `keys/keybindings.md` standard | [P02-sandbox-and-keybindings.md](plans/P02-sandbox-and-keybindings.md) | Done (2026-11-25) |
| **PH03** | 1.3.0 | Standardize `ROADMAP.md` format, enforce in `idol-check`, and roll out across all repos | [P03-roadmap-standard.md](plans/P03-roadmap-standard.md) | Done (2026-11-26) |
| **PH04** | 1.4.0 | Separate phase and plan IDs while supporting legacy roadmaps | [P04-phase-identifiers.md](plans/P04-phase-identifiers.md) | In progress |

## Phases and milestones

### Phase PH01: The standard and initial rollout (0.1.0–1.0.0) — [P01-standard.md](plans/P01-standard.md)

| Version | Milestone | Status |
| --- | --- | --- |
| **0.1.0** | Standard set, six `README-<folder>` templates, procedures in `README`, `tools/idol-check`, and `tam-clif` pilot | Done (2026-11-18) |
| **0.2.0** | Work history moves under `work/` (`W<n>-<name>` and `work/history/`); retire `docs/ai/` | Done (2026-11-20) |
| **0.2.1** | Allow `work/ai-blame-standard.md` in `tamlinux` and `tools/idol-check` | Done (2026-11-20) |
| **1.0.0** | Every Tamlinux repository passes `tools/idol-check`; branches unified on `dev`, `AI-BLAME.md` everywhere, and `tamlinux` reorganized | Done (2026-11-20) |

### Phase PH02: Sandbox and shared keybindings (1.1.0–1.2.1) — [P02-sandbox-and-keybindings.md](plans/P02-sandbox-and-keybindings.md)

| Version | Milestone | Status |
| --- | --- | --- |
| **1.1.0** | Add optional `sandbox/` folder (`sandbox/README-sandbox`) and validate in `tools/idol-check` | Done (2026-11-21) |
| **1.2.0** | Add shared keybinding standard in `keys/keybindings.md` | Done (2026-11-25) |
| **1.2.1** | Move per-program keybinding documentation into `keys/keybindings.md` with `keys/README-keys` | Done (2026-11-25) |

### Phase PH03: Standard ROADMAP.md format (1.3.0) — [P03-roadmap-standard.md](plans/P03-roadmap-standard.md)

| Version | Milestone | Status |
| --- | --- | --- |
| **1.3.0** | Define `arch/roadmap.md`, enforce `ROADMAP.md` structure and plan links in `tools/idol-check`, and update every repository | Done (2026-11-26) |

### Phase PH04: Separate phase and plan IDs (1.4.0) — [P04-phase-identifiers.md](plans/P04-phase-identifiers.md)

| Version | Milestone | Status |
| --- | --- | --- |
| **1.4.0** | Specify PHxx phase order and stable Pxx plan IDs, teach `idol-check` both formats, and migrate tam-idol and tamlinux | In progress |

## How a milestone is done

A milestone is done when its acceptance checks in the phase plan pass and
Fred has accepted the change. When a milestone lands, bump `VERSION`,
update the phase plan's status, and update this roadmap in the same
change.
