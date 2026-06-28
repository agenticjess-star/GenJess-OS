---
name: agents
 description: Core guidelines, anti-patterns, and operational principles for all agents working in GenJess-OS. Read this before executing any significant work.
---

# AGENTS.md — GenJess-OS

This document contains critical information for any agent operating inside GenJess-OS.

## Core Principles

- **Ship projects, not just messages.** Every action should move toward a shippable outcome.
- **Own the Outcome.** Take full responsibility for the quality and completeness of your work.
- **Evidence First.** Gather and log evidence before making strong claims or recommendations.
- **Progressive Disclosure.** Load only the context you need. Prefer small, focused files over monolithic context.

## Anti-Patterns to Avoid

- Do not make changes without understanding the existing structure and intent.
- Do not skip verification steps (especially for code, data, or external actions).
- Do not assume you have the full picture — always check relevant `README.md` / `AGENTS.md` files in folders you touch.
- Avoid large, unfocused changes when smaller, targeted ones will suffice.

## Operational Rules

1. Always check the relevant folder's `README.md` or `AGENTS.md` before working in it.
2. Prefer creating or updating small, focused files over editing large ones.
3. Log important decisions and evidence in the shared state (Supabase / workspace).
4. When in doubt, ask clarifying questions or propose small experiments.

## File Naming Conventions

- `README.md` — Human-oriented overview of a folder or project.
- `AGENTS.md` — Agent-specific guidelines, anti-patterns, and important context.
- `SKILL.md` — Reusable agent skill following the standard Agent Skills format.
- `STRUCTURE.md` — Technical or architectural overview (when needed).

## Recommended Reading Order

1. Root `README.md`
2. This `AGENTS.md`
3. Relevant subfolder `README.md` or `AGENTS.md`
4. Specific skill files when using tools