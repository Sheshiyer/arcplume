# Changelog

All notable changes to Arcplume are documented in this file.

## [1.0.0] - 2026-05-25

### Added
- Initial public release of **Arcplume** skill.
- Hardened cookie-auth workflow for signed-in X account usage (`AUTH_TOKEN` + `CT0`).
- Strict auth resolution order: env -> `~/.claude/.env` -> `~/.config/bird/config.json5`.
- Mandatory preflight validation with `bird whoami`.
- Browser-first execution path for account-bound Grok behavior.
- Explicit API mode boundary (opt-in only).
- Secret-safe constraints and failure messaging template.
- Helper scripts:
  - `scripts/load-cookies.sh`
  - `scripts/preflight.sh`
  - `scripts/test-video.sh`
- Branding assets and Arcplume icon set.
- CI workflow to validate `SKILL.md` frontmatter/body presence.

### Notes
- Re-imagined and renamed from the earlier concept into **Arcplume**.
