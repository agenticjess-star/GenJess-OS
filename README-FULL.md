# GenJess-OS

**Production Agent Operating System for the GenJess Agency**

GenJess-OS is the robust, production-grade agent operating system that powers the GenJess agency. It runs the 7-agent Outbound Studio crew, executes reliable deployments via the improved Deploy Pipeline, uses **AxonAI** as the primary human + agent collaboration surface, and enforces **Own-the-Outcome** workflows so every deliverable is fully owned, verified, and exceptional.

## Core Principles

1. **Own the Outcome** — For any complex request, the system clarifies true intent and success criteria, focuses on high-leverage elements, plans thoroughly, executes autonomously, self-reviews & iterates until exceptional quality, then delivers a complete, polished outcome that the agent fully owns and stands behind.
2. **Agent-First + Skills-First** — Specialized agents. `skills/` is the canonical workflow surface.
3. **Verification-First + TDD** — Byte-level + live verification on every deploy/output. TDD is mandatory.
4. **Reliable Communication Outside Chat** — Primary: MCP + Supabase shared state + AxonAI workspace. Slack/Telegram = notifications & human approvals only.
5. **Token & Context Optimization** — Subagent delegation to cheapest sufficient model, iterative retrieval (max 3 cycles), strategic compacting.
6. **Memory & Continuous Learning** — PreCompact/Stop/SessionStart hooks + continuous learning skill that appends non-trivial discoveries directly into skills.
7. **Lean + Explain the Why** — Fewer, better instructions. Every rule includes causal reasoning.
8. **Immutability + Security-First + Plan Before Execute**

## Architecture

```
GenJess-OS
├── agents/
│   ├── outbound-crew/          # 7 agents with Own-the-Outcome gates
│   ├── core/                   # planner, tdd-guide, code-reviewer, security-reviewer, loop-operator...
│   └── domain/
├── skills/                     # Canonical surface
│   ├── own-the-outcome/        # Meta-workflow (clarify → plan → execute → self-review → deliver)
│   ├── deploy-pipeline/        # Improved (lean docs, common.py, MCP wrapper, self-review gate)
│   ├── continuous-learning/    # Auto-appends discoveries to skills
│   ├── axonai-integration/     # Tasks, kanban, group chat in AxonAI workspace
│   └── verification/
├── mcp-servers/                # Standardized tool calling (Deploy Pipeline, GitHub, Vercel, Supabase...)
├── shared-state/               # Supabase (tasks, workflow_state, session_summaries, learnings)
├── orchestration/              # Phase-based flows + iterative retrieval + human gates
├── axonaut/                    # AxonAI workspace as primary human + agent collaboration surface
└── hooks/
    └── memory-persistence/
```

## Key Components

### Own-the-Outcome Skill (First-Class Meta-Workflow)
Activated automatically for complex work. Enforces:
- Intent clarification & success criteria definition
- High-leverage planning only
- Autonomous execution via skills/MCP
- Self-review + iteration until exceptional
- Complete delivery (live result + verification report + knowledge capture)

### 7-Agent Outbound Studio with Ownership Gates
The **Conductor** owns the final outcome for every run. No handoff is accepted until it meets the defined success criteria.

### Improved Deploy Pipeline
- Lean documentation (no duplication)
- `scripts/common.py` (bundled API/retry patterns)
- MCP server wrapper for clean agent invocation
- Built-in self-review + outcome gate after verification
- Still performs atomic Git Data API commits + full byte + live verification

### Reliable Communication Layer (Outside Slack)
**Primary (robust & durable):**
- MCP servers for tool calling
- Supabase for persistent tasks, state, and knowledge
- AxonAI workspace for group chat, tasks, and kanban between agents + humans

**Secondary (notifications & approvals only):**
- Slack (Block Kit)
- Telegram

### Memory & Continuous Learning
- Per-session summary files in `.claude/sessions/`
- PreCompact / Stop / SessionStart hooks
- Continuous learning skill that automatically turns non-trivial discoveries into new or updated skills

### Token Optimization & Parallelization
- Subagent delegation by task type
- Iterative retrieval pattern
- Git worktrees + named chats + cascade method
- Strategic compacting at phase boundaries

## Project Structure

`skills/` is the canonical workflow surface. All new reusable patterns land here first.

## Getting Started

1. Clone the repo
2. Configure your MCP servers and Supabase connection
3. Run the Outbound Studio crew via the Conductor (Own-the-Outcome mode activates automatically)
4. All complex work follows the full ownership process

## Roadmap

- [x] Repo created + initial README
- [ ] Full `skills/own-the-outcome/` implementation
- [ ] Deploy Pipeline MCP server + `common.py`
- [ ] Memory persistence hooks
- [ ] AxonAI integration skill
- [ ] First production run of the 7-agent crew with full verification

---

**GenJess-OS ships excellence. Every outcome is owned.**