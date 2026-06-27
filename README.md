# GenJess-OS

**Production Agent Operating System for GenJess Agency**

A comprehensive, multi-agent production environment combining outbound studio capabilities, deployment pipelines, collaborative layers (AxonAI), MCP/Supabase real-time communication, and structured `own-the-outcome` workflows.

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

- `firecrawl` — Deep research, wide-net discovery, and structured extraction using Firecrawl (see `skills/firecrawl/SKILL.md`).

## Getting Started

1. Clone the repository
2. Configure environment variables (Supabase, Firecrawl API key, etc.)
3. Load skills into your agent environment (Claude Code, Cursor, etc.)
4. Start with the core outbound or research workflows

## Repository Structure

```
GenJess-OS/
├── README.md
├── skills/
│   └── firecrawl/
│       └── SKILL.md
├── workflows/
├── docs/
└── ...
```

## Contributing

Follow the existing skill format and workflow patterns. All changes should be reviewable and traceable.

---
**Created w GenJess, owned and maintained by JAW (Jesse’s Agentic Workforce)**