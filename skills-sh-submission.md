# Arcplume — skills.sh Submission Metadata

## Basic
- **Name:** Arcplume
- **Slug:** `arcplume`
- **Tagline:** Grok via your local signed-in X session, safely.
- **Category:** Productivity / Automation / Social
- **Homepage:** https://github.com/Sheshiyer/arcplume
- **License:** MIT

## Short Description
Arcplume runs Grok through a locally signed-in X account using cookie credentials (`AUTH_TOKEN`/`CT0`) with strict preflight validation, secret-safe handling, and browser-first execution.

## Long Description
Arcplume is a hardened skill for users who explicitly want signed-account Grok behavior (cookie/session mode), not accidental API-key mode. It resolves credentials safely, validates account context with `bird whoami`, enforces no-secret-leak constraints, and executes through browser-first Grok flows where account-bound behavior is most reliable.

## Key Features
- Cookie/session-first execution (`AUTH_TOKEN` + `CT0`)
- Strict preflight and remediation messages
- Browser-first for signed-account workflows
- Explicit opt-in for API mode (`XAI_API_KEY`)
- Repeatable video endpoint smoke test (`scripts/test-video.sh`)

## Trigger Phrases
- "use grok with my local account"
- "use auth_token and ct0"
- "use cookies from .claude/.env"
- "run through signed-in X account"

## Install
```bash
mkdir -p ~/.craft-agent/workspaces/my-workspace/skills/arcplume
cp SKILL.md ~/.craft-agent/workspaces/my-workspace/skills/arcplume/SKILL.md
craft-agent skill validate arcplume
```

## Repo Assets
- Skill: `SKILL.md`
- Icon: `icon.png`
- Security policy: `SECURITY.md`
- Preflight helper: `scripts/preflight.sh`
- Video smoke test: `scripts/test-video.sh`

## Suggested Tags
`grok`, `x`, `automation`, `cookie-auth`, `security`, `browser-automation`, `xai`
