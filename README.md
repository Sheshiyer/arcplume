<div align="center">

# 🪶 Arcplume

**Hardened skill for running Grok through your locally signed-in X account** using cookie credentials (`AUTH_TOKEN` + `CT0`) with strict preflight checks.

![License](https://img.shields.io/github/license/Sheshiyer/arcplume?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/Sheshiyer/arcplume?style=flat-square)
![Repo Size](https://img.shields.io/github/repo-size/Sheshiyer/arcplume?style=flat-square)

</div>

---

<div align="center">

<img src="./icon.png" alt="Arcplume icon" width="128" />

</div>

## Why this exists

Most Grok automations confuse API mode and signed-account mode. This skill makes the session-backed workflow explicit and safe:

- ✅ Cookie/session-first execution
- ✅ Preflight auth validation before any task
- ✅ Browser-first path for account-bound behavior
- ✅ Strict no-secret-leak policy

---

## Install

Copy this skill into your Craft workspace skills folder:

```bash
mkdir -p ~/.craft-agent/workspaces/my-workspace/skills/arcplume
cp SKILL.md ~/.craft-agent/workspaces/my-workspace/skills/arcplume/SKILL.md
```

Then validate:

```bash
craft-agent skill validate arcplume
```

---

## Credentials (safe loading order)

1. Environment variables (`AUTH_TOKEN`, `CT0`)
2. `~/.claude/.env`
3. `~/.config/bird/config.json5`

The skill never prints raw token values.

---

## Preflight check

```bash
scripts/preflight.sh
```

Expected result: `bird whoami` succeeds with cookie credentials.

---

## Rebrand exploration (May 2026)

Fresh icon/name concepts live in [`branding/rebrand-2026-05/icons`](./branding/rebrand-2026-05/icons).
Current `icon.png` is set to the **Arcplume** concept for review.

## Security hardening

See [SECURITY.md](./SECURITY.md) for:
- threat model
- secret handling rules
- incident response checklist

---

## Repo layout

```text
.
├── SKILL.md
├── README.md
├── SECURITY.md
├── scripts/
│   ├── load-cookies.sh
│   └── preflight.sh
└── .github/workflows/
    └── validate-skill.yml
```

---

## Publish to skills.sh checklist

- [x] Valid SKILL frontmatter
- [x] Clear trigger conditions
- [x] Safety/constraints documented
- [x] Security guidance included
- [x] Basic CI validation workflow


---

## Brand update

This project was re-imagined and renamed from **Grok Account Bridge** to **Arcplume**.
