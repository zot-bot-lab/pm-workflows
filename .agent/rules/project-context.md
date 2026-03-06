---
description: Project context and configuration for pm-agent-workflows
---

# PM Agent Workflows

This project contains agent workflows for project management automation across GitHub organizations.

## GitHub Organizations

| Role | Org Login | Notes |
|------|-----------|-------|
| **Main** (destination) | `team-zeroone` | Central project board — ZOT Team |
| **Secondary** (source) | `zot-bot-lab` | Individual product boards |

## Project Boards

| Board | Org | Project # |
|-------|-----|-----------|
| ZOT Team (Main) | `team-zeroone` | 31 |
| Clockify Discord Reporter Product Board | `zot-bot-lab` | 1 |

## Project Structure

- **`.agent/rules/`** — AI agent rules & context
- **`.agent/workflows/`** — Slash command definitions (triggers only)
- **`scripts/`** — All executable automation scripts and their configs
- **`changelogs/`** — Auto-generated run logs per workflow
- **`README.md`** — Project documentation

## Important Rules

1. **Never delete items** on any project board.
2. **Never modify** the secondary board — it is read-only for sync purposes.
3. **Statuses** across all boards: Backlog, Ready, In progress, In review, Done, Blocked, Discarded.
4. **Iteration field** is named "Week" on all boards.
5. **After every workflow run**, update `README.md` at the project root to reflect any new workflows, boards, or structural changes.

