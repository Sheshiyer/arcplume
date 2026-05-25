<div align="center">

# 🪽 Arcplume

**Run Grok through your local signed-in X session** with hardened cookie auth (`AUTH_TOKEN` + `CT0`), strict preflight checks, and browser-first execution.

![License](https://img.shields.io/github/license/Sheshiyer/arcplume?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/Sheshiyer/arcplume?style=flat-square)
![Repo Size](https://img.shields.io/github/repo-size/Sheshiyer/arcplume?style=flat-square)
![Release](https://img.shields.io/github/v/release/Sheshiyer/arcplume?style=flat-square)

<img src="./icon.png" alt="Arcplume icon" width="128" />

</div>

---

## Why Arcplume

Most Grok automations blur two very different modes:
- **Cookie-backed signed-account mode** (what users actually asked for)
- **API-key mode** (`XAI_API_KEY`)

Arcplume keeps that boundary explicit and safe.

### Core guarantees
- ✅ Cookie/session-first behavior
- ✅ Mandatory `bird whoami` preflight before execution
- ✅ Browser-first flow for account-bound tasks
- ✅ No secret echo in output/logs
- ✅ No silent fallback from cookie mode to API mode

---

## Install

```bash
mkdir -p ~/.craft-agent/workspaces/my-workspace/skills/arcplume
cp SKILL.md ~/.craft-agent/workspaces/my-workspace/skills/arcplume/SKILL.md
craft-agent skill validate arcplume
```

---

## Credential resolution order

Arcplume loads credentials in this order:

1. Process env (`AUTH_TOKEN`, `CT0`)
2. `~/.claude/.env`
3. `~/.config/bird/config.json5`

Raw token values are never printed.

---

## Quick preflight

```bash
scripts/preflight.sh
```

Expected result: cookie-authenticated `bird whoami` success.

---

## Repeatable endpoint tests

### Video endpoint smoke test

```bash
scripts/test-video.sh \
  --prompt "Arcplume logo reveal, dark bg, cyan-violet glow, no text" \
  --duration 5 \
  --out ./arcplume-teaser.mp4
```

---

## Security

Read [SECURITY.md](./SECURITY.md) for threat model, secret handling rules, and incident response guidance.

---

## Branding assets

Rebrand concepts and social teaser notes:
- [branding/rebrand-2026-05/icons](./branding/rebrand-2026-05/icons)
- [branding/rebrand-2026-05/teasers/README.md](./branding/rebrand-2026-05/teasers/README.md)

---

## skills.sh publish checklist

- [x] Valid frontmatter (`name`, `description`)
- [x] Hardened auth and safety constraints
- [x] Helper scripts for preflight and endpoint tests
- [x] Repo-level CI validation
- [x] Icon + brand assets
- [x] Release metadata prepared

See [skills-sh-submission.md](./skills-sh-submission.md) for copy-paste listing metadata.
