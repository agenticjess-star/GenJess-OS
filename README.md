# GenJess-OS

**Production Agent Operating System for GenJess Agency**

A comprehensive, multi-agent production environment combining outbound studio capabilities, deployment pipelines, collaborative layers (AxonAI), MCP/Supabase real-time communication, and structured `own-the-outcome` workflows.

## Quick Navigation

- [AGENTS.md](https://raw.githubusercontent.com/agenticjess-star/GenJess-OS/main/AGENTS.md) — Critical guidelines for agents
- [STRUCTURE.md](https://raw.githubusercontent.com/agenticjess-star/GenJess-OS/main/STRUCTURE.md) — Technical architecture overview
- [skills/firecrawl/SKILL.md](https://raw.githubusercontent.com/agenticjess-star/GenJess-OS/main/skills/firecrawl/SKILL.md) — Firecrawl research skill

## Repository Structure

```
GenJess-OS/
├── README.md                 # Human overview (this file)
├── AGENTS.md                 # Agent guidelines & anti-patterns
├── STRUCTURE.md              # Technical architecture
├── README-FULL.md            # Extended/detailed version
├── .claude/                  # Claude Code configuration
├── agents/                   # Agent definitions & orchestration
├── axonaut/                  # AxonAI collaboration layer
├── hooks/                    # Automation hooks
├── mcp-servers/              # MCP server configurations
├── orchestration/            # Workflow orchestration logic
└── skills/                   # Reusable agent skills
    └── firecrawl/            # Firecrawl research & extraction skill
```

## Overview

GenJess-OS is designed as a full agent operating system. It orchestrates multiple specialized agents that can plan, execute, review, and ship work with high reliability and traceability.

Core principles:
- **Ship projects, not just messages**
- Structured workflows with clear verification steps
- Persistent shared state via Supabase + MCP
- Composable skills following the Agent Skills specification
- Strong separation between planning, execution, and review

## Architecture

- **7-Agent Outbound Studio**: Specialized agents for different stages of outbound work.
- **Deploy Pipeline**: Automated testing, building, and deployment workflows.
- **AxonAI Collaboration Layer**: Connective tissue for human + agent coordination.
- **MCP + Supabase**: Real-time state synchronization and tool calling.
- **Own-the-Outcome Workflows**: Evidence-first, high-accountability processes.

## Skills System

This repository follows the standard Agent Skills format (`SKILL.md` with YAML frontmatter + instructions).

Skills live in the `skills/` directory. Each skill is self-contained and discoverable.

### Current Skills

- `firecrawl` — Deep research, wide-net discovery, and structured extraction using Firecrawl.

## Getting Started

1. Clone the repository
2. Configure environment variables (Supabase, Firecrawl API key, etc.)
3. Load skills into your agent environment (Claude Code, Cursor, etc.)
4. Start with the core outbound or research workflows

## Contributing

Follow the existing skill format and workflow patterns. All changes should be reviewable and traceable.

---
**Created w GenJess, owned and maintained by JAW (Jesse’s Agentic Workforce)**