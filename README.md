# PM Agent Workflows

A collection of automated workflows for managing GitHub Project Boards across multiple organizations.

## Available Workflows

### `/sync-boards` - Project Board Sync
Syncs tasks from secondary project boards to the main **team-zeroone** (#31) board.

**Run manually:**
```powershell
powershell -ExecutionPolicy Bypass -File scripts/sync-boards/sync-boards.ps1
```

**What it syncs:** Status, Week, Priority, Size, Estimate, Start date, Target date (→ End date)

**Config:** `scripts/sync-boards/sync-config.json`

**Run logs:** `changelogs/sync-boards.md`

## Project Structure
```
pm-agent-workflows/
├── .agent/
│   ├── rules/          # AI agent rules & context
│   └── workflows/      # Slash command definitions
├── changelogs/          # Auto-generated run logs per workflow
├── scripts/
│   └── sync-boards/    # Sync engine + config
└── README.md
```
