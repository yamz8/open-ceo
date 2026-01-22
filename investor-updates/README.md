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

## Configuration (Optional)

Create `.claude/investor-updates.local.md` in your project for personalized updates:

```yaml
---
company_name: "Your Company"
stage: "Series A"
investors:
  - name: "Jane Smith"
    firm: "Acme Ventures"
    email: "jane@acmeventures.com"
metrics:
  arr: "$2.4M"
  mrr_growth: "8%"
  runway: "18 months"
---
```

**No configuration?** No problem - the plugin will ask for details when needed.

**Using other Open CEO plugins?** This plugin can also read from `.claude/board-prep.local.md` or `.claude/metrics.local.md` if they exist, so you don't need to duplicate information.

## Metrics Tracked

Lighter subset of SaaS metrics for monthly updates:
- ARR / MRR and growth rates
- Key wins and milestones
- Runway update
- Team highlights

## Installation

Add to your Claude Code settings or use via the open-ceo marketplace.
