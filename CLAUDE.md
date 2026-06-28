# CLAUDE.md — GenJess-OS

Production agent operating system for GenJess agency.

**7-agent Outbound Studio** + **Deploy Pipeline** + **AxonAI collab layer** + **MCP/Supabase** + **own-the-outcome workflows**.

This is the canonical context file for Claude Code and other harnesses (Codex, Cursor, OpenCode, Gemini CLI).

> Read this like a table of contents. Detail lives in linked files.

## Map

- [README.md](README.md) — Human overview + repository structure
- [AGENTS.md](AGENTS.md) — Agent guidelines, anti-patterns, and operational rules
- [skills_index.json](skills_index.json) — Index of all reusable skills
- [skills/firecrawl/SKILL.md](skills/firecrawl/SKILL.md) — Firecrawl research skill
- [skills/deploy-pipeline/SKILL.md](skills/deploy-pipeline/SKILL.md) — Full deploy pipeline (GitHub + Vercel + verification + media + email)
- [charters/outbound-studio-charter.md](charters/outbound-studio-charter.md) — Outbound Studio business model and agent topology
- [charters/axonai-agency-charter.md](charters/axonai-agency-charter.md) — AxonAI Agency master charter (market, product, revenue)

## Core Principles

- **Ship projects, not just messages**
- **Own the Outcome** — full responsibility for quality and completeness
- **Evidence First** — gather and log evidence before strong claims
- **Progressive Disclosure** — load only what you need
- **Template-first production** — retrieve, adapt, assemble, verify (never free-code when a component exists)

## Quality Gates

Before committing changes:
- Run relevant skill verification
- Update `skills_index.json` if adding/removing skills
- Keep `AGENTS.md` and `CLAUDE.md` lean and accurate

## Working in this repo

- Skills live under `skills/<name>/SKILL.md` following the standard Agent Skills spec
- Charters and long-form strategy live under `charters/`
- Keep root files short and navigational

## Next Priorities

- Flesh out `skills/deploy-pipeline/SKILL.md` from the v3 export
- Create folder-level README.md / AGENTS.md in `skills/`, `agents/`, `orchestration/`
- Expand AxonAI Business OS features (Lead View, Review Monitor, Email integration)