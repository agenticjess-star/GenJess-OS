# Memory Persistence Hooks

## Hooks
- **PreCompact**: Save important state before context compaction
- **Stop**: On session end, create session summary + trigger continuous learning
- **SessionStart**: Load previous relevant session summaries

## Location
`.claude/sessions/` for per-session outcome files.