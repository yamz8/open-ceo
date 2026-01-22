# Fundraising Plugin

A comprehensive fundraising toolkit for VC-backed startup CEOs. Part of the [Open CEO](https://github.com/yamz8/open-ceo) marketplace.

## Features

- **Pitch Deck Generation**: Create deck outlines in Sequoia, YC, or a16z formats
- **Investor Outreach**: Draft cold emails, warm intro requests, and follow-up sequences
- **Term Sheet Analysis**: Analyze terms, compare offers, identify red flags
- **Due Diligence Prep**: Stage-appropriate checklists and data room organization
- **Pipeline Tracking**: Light CRM for managing investor conversations

## Installation

```bash
# Install via Claude Code marketplace
claude mcp add marketplace:fundraising@open-ceo
```

Or add manually to your Claude Code configuration.

## Commands

| Command | Description |
|---------|-------------|
| `/pitch-deck [format] [stage]` | Generate pitch deck outline |
| `/outreach [type] [investor]` | Create investor emails |
| `/term-sheet [action]` | Analyze or compare term sheets |
| `/due-diligence [stage]` | Generate DD checklist |
| `/pipeline [action] [investor]` | Manage investor pipeline |

### Examples

```bash
# Generate a Sequoia-format deck for Series A
/pitch-deck sequoia series-a

# Create a cold outreach email
/outreach cold "Sarah at Acme Ventures"

# Analyze a term sheet
/term-sheet analyze

# Compare two term sheets
/term-sheet compare

# Get DD checklist for seed round
/due-diligence seed

# View pipeline summary
/pipeline summary

# Add investor to pipeline
/pipeline add "Acme Ventures"
```

## Configuration (Optional)

For personalized guidance, create `.claude/fundraising.local.md` with your company details:

```yaml
---
company_name: "Your Company"
one_liner: "What you do in one sentence"
stage: "seed"
arr: 500000
mrr_growth: 15
raise_amount: 3000000
---

## Company Context
[Additional context about your company...]
```

See `examples/fundraising.local.example.md` for a complete template.

## Stages Supported

- **Pre-seed**: SAFE/convertible focus, team + vision emphasis
- **Seed**: Early traction, product-market fit signals
- **Series A**: Proven PMF, repeatable GTM
- **Series B+**: Scale, unit economics, path to profitability

## What's Included

### Skill: Fundraising Knowledge
Comprehensive knowledge base covering:
- Pitch deck templates (Sequoia, YC, a16z formats)
- Stage-specific guidance and benchmarks
- Term sheet glossary and red flags
- Outreach best practices and sequences

### Agent: Fundraising Assistant
Proactive assistant that activates when you're working on:
- Investor communications
- Pitch decks and presentations
- Term sheet review
- Meeting preparation

## Related Plugins

This plugin is part of the Open CEO ecosystem:

```
Fundraising → Board Prep → Investor Updates
```

- **[Board Prep](../board-prep)**: Prepare for board meetings
- **[Investor Updates](../investor-updates)**: Send monthly investor updates

## License

MIT
