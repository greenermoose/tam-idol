# P02: Sandbox and shared keybinding standards

- **Status:** done (2026-11-25)
- **Versions:** 1.1.0 to 1.2.1

## Goal

Extend the `tam-idol` standard after 1.0.0 with an optional `sandbox/`
folder for demos and manual testing and a shared `keys/keybindings.md`
standard for every Tamlinux program with keyboard controls.

## Versions

- **1.1.0 (done 2026-11-21):** Add `sandbox/` (`sandbox/README-sandbox`)
  as an optional standard folder and check it in `tools/idol-check`
  whenever a repository has `sandbox/` (W15).
- **1.2.0 (done 2026-11-25):** Add `keys/keybindings.md` as the shared
  keybinding standard for all Tamlinux programs (W17).
- **1.2.1 (done 2026-11-25):** Standardize per-program keybinding docs
  in `keys/keybindings.md` (with `keys/README-keys`) instead of
  `arch/keys.md` (W18).

## Acceptance

- `tools/idol-check` validates `sandbox/README-sandbox` when `sandbox/`
  exists and documents `keys/keybindings.md` in `--list`.
- `tam-idol` itself passes `tools/idol-check`.

## Dependencies

None.

## Risks

None (completed).

## Open points

None.
