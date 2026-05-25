# Arcplume v1.0.0

Arcplume is now live as a hardened, publish-ready skill for running Grok through a **local signed-in X session** safely and predictably.

## Highlights
- Signed-account cookie mode first (`AUTH_TOKEN` + `CT0`)
- Mandatory preflight checks before execution
- Browser-first default for account-bound tasks
- Strict no-secret-leak constraints
- Explicit separation of cookie mode vs API mode

## Included in this release
- `SKILL.md` (production-ready skill definition)
- `README.md` (skills.sh-focused documentation)
- `SECURITY.md` (threat model and incident response)
- `scripts/preflight.sh` and `scripts/load-cookies.sh`
- `scripts/test-video.sh` for repeatable video endpoint checks
- Arcplume icon + rebrand assets

## Quick start
```bash
mkdir -p ~/.craft-agent/workspaces/my-workspace/skills/arcplume
cp SKILL.md ~/.craft-agent/workspaces/my-workspace/skills/arcplume/SKILL.md
craft-agent skill validate arcplume
```

## Acknowledgements
Built with and powered by Craft Agent workflows.
