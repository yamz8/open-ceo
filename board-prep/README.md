# Board Prep Plugin

A Claude Code plugin to help VC-backed startup CEOs prepare for board meetings.

## Features

- **Full prep workflow** - Guided process from start to finish
- **Agenda creation** - Generate professional board meeting agendas
- **Board deck drafting** - Create structured markdown decks with SaaS metrics
- **Q&A preparation** - Anticipate and prepare for tough investor questions
- **Proactive assistance** - Agent helps when board prep tasks are detected

## Commands

| Command | Description |
|---------|-------------|
| `/board-prep:start` | Kick off the full board prep workflow |
| `/board-prep:agenda` | Generate a board meeting agenda |
| `/board-prep:deck` | Draft board deck sections |
| `/board-prep:qa-prep` | Prepare for anticipated questions |

## Configuration

Create `.claude/board-prep.local.md` in your project to store company-specific information:

```markdown
---
company_name: Your Company
board_members:
  - name: Jane Smith
    role: Lead Investor
    firm: Acme Ventures
  - name: John Doe
    role: Independent Director
meeting_cadence: quarterly
---

## Key Metrics Sources
- Revenue data: spreadsheet.csv
- User metrics: analytics dashboard

## Previous Board Materials
- Last deck: docs/board-deck-q3.md
```

## Metrics Tracked

Standard SaaS metrics included:
- ARR / MRR and growth rates
- Churn (gross and net)
- CAC and LTV
- Burn rate and runway
- Headcount

## Installation

Add to your Claude Code settings or use via the open-ceo marketplace.
