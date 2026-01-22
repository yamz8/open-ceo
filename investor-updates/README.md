# Investor Updates Plugin

A Claude Code plugin to help VC-backed startup CEOs send professional monthly investor updates.

## Features

- **Draft updates** - Generate complete investor email drafts or markdown outlines
- **Metrics snapshots** - Quick metrics summary for your update
- **Send checklist** - Pre-send verification for recipients, tone, and data accuracy
- **Proactive assistance** - Agent helps when investor update work is detected

## Commands

| Command | Description |
|---------|-------------|
| `/investor-updates:draft` | Draft a monthly investor update email |
| `/investor-updates:metrics` | Generate a metrics snapshot for the update |
| `/investor-updates:send-checklist` | Pre-send checklist before sending |

## Configuration

This plugin shares configuration with the board-prep plugin. Create or update `.claude/board-prep.local.md` in your project:

```markdown
---
company_name: Your Company
stage: Series A
board_members:
  - name: Jane Smith
    role: Lead Investor
    firm: Acme Ventures
    email: jane@acmeventures.com
---

## Key Metrics Sources
- Revenue data: spreadsheet.csv
- User metrics: analytics dashboard
```

## Metrics Tracked

Lighter subset of SaaS metrics for monthly updates:
- ARR / MRR and growth rates
- Key wins and milestones
- Runway update
- Team highlights

## Installation

Add to your Claude Code settings or use via the open-ceo marketplace.
