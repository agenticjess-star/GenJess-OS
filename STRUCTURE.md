# GenJess-OS Project Structure

This is the canonical structure for the production agent operating system.

```
GenJess-OS/
├── README.md                    # Short public README
├── README-FULL.md               # Complete detailed design (this is the gold standard version)
├── STRUCTURE.md                 # This file
├── agents/
│   ├── outbound-crew/          # 7-agent Outbound Studio
│   ├── core/                   # General agents (planner, reviewer, etc.)
│   └── domain/                 # Domain-specific agents
├── skills/                     # Canonical workflow surface
│   ├── own-the-outcome/        # Meta ownership workflow
│   ├── deploy-pipeline/        # Core deployment engine
│   ├── continuous-learning/    # Auto skill improvement
│   ├── axonai-integration/     # AxonAI workspace integration
│   └── verification/           # Byte + live + outcome verification
├── mcp-servers/                # MCP tool definitions
├── shared-state/               # Supabase schema docs
├── orchestration/              # Crew flow graphs & phase logic
├── axonaut/                    # AxonAI workspace customizations
├── hooks/
│   └── memory-persistence/     # PreCompact, Stop, SessionStart hooks
├── .claude/
│   ├── contexts/               # Dynamic system prompts
│   └── sessions/               # Per-session outcome summaries
└── docs/                       # Additional documentation
```