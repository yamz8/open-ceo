# Startup CEO Marketplace for Claude Code

This marketplace provides plugins for VC-backed startup CEOs. Install these plugins to access AI-powered tools for fundraising, board meeting preparation, and investor communication directly within Claude Code.

**What's included:**
- **Commands**: Structured workflows for pitch decks, board decks, and investor updates
- **Agents**: Proactive assistants that trigger automatically when working on fundraising, board prep, or investor communication
- **Skills**: Domain-specific knowledge for fundraising, board meetings, and investor relations

## The CEO Workflow

```
Fundraising → Board Prep → Investor Updates
     ↑                           |
     └───── Next Round ←─────────┘
```

## Quick Start

```bash
# Add the marketplace
/plugin marketplace add yamz8/open-ceo

# Install plugins
/plugin install fundraising@open-ceo
/plugin install board-prep@open-ceo
/plugin install investor-updates@open-ceo
```

After installation, configure your company context (see Configuration section below).

## Available Plugins

### Fundraising
**Plugin ID**: `fundraising@open-ceo`

Complete fundraising toolkit for VC-backed startup CEOs. Create pitch decks, write investor outreach, analyze term sheets, and manage your fundraising pipeline.

**Commands:**
| Command | Description |
|---------|-------------|
| `/pitch-deck [format] [stage]` | Generate pitch deck outline (Sequoia, YC, a16z formats) |
| `/outreach [type] [investor]` | Create investor emails (cold, warm, follow-up) |
| `/term-sheet [action]` | Analyze or compare term sheets |
| `/due-diligence [stage]` | Generate DD checklist by stage |
| `/pipeline [action]` | Track investor pipeline |

**Features:**
- Pitch deck templates for Sequoia, YC, and a16z formats
- Cold/warm outreach email sequences
- Term sheet analysis with red flag detection
- Stage-specific due diligence checklists (pre-seed to Series C)
- Light investor pipeline CRM

**Requirements**: None - works with any project

---

### Board Prep
**Plugin ID**: `board-prep@open-ceo`

Comprehensive board meeting preparation toolkit for VC-backed startup CEOs. Create professional board decks, agendas, and prepare for investor Q&A.

**Commands:**
| Command | Description |
|---------|-------------|
| `/board-prep:start` | Full board prep workflow with checklist |
| `/board-prep:agenda` | Generate professional board meeting agenda |
| `/board-prep:deck` | Draft board deck sections in markdown |
| `/board-prep:qa-prep` | Prepare for anticipated investor questions |

**Features:**
- 10-section board deck generation (summary, metrics, business updates, financials, GTM, product, team, strategic, asks, appendix)
- SaaS metrics tracking (ARR, MRR, growth rates, churn, CAC, LTV, burn rate, runway)
- Investor Q&A preparation across 5 focus areas
- Configurable agenda formats (90-min, 2-hour, 3-hour)

**Requirements**: None - works with any project

### Investor Updates
**Plugin ID**: `investor-updates@open-ceo`

Monthly investor communication assistant. Draft professional investor updates optimized for busy investors.

**Commands:**
| Command | Description |
|---------|-------------|
| `/investor-updates:draft` | Draft monthly investor update |
| `/investor-updates:metrics` | Generate metrics snapshot |
| `/investor-updates:send-checklist` | Pre-send verification checklist |

**Features:**
- Structured update format (TL;DR, Highlights, Metrics, Challenges, Asks, Looking Ahead)
- 2-3 minute read optimization (300-500 words)
- Email or markdown output formats
- 20+ item pre-send checklist across 6 categories

**Requirements**: None - works with any project

## Detailed Installation

### 1. Add the marketplace (one time)

```bash
/plugin marketplace add https://github.com/yamz8/open-ceo.git
```

### 2. Install specific plugins

```bash
# Install all three for the complete CEO workflow
/plugin install fundraising@open-ceo
/plugin install board-prep@open-ceo
/plugin install investor-updates@open-ceo
```

### 3. Configure company context (optional)

Each plugin can use its own configuration file for personalized output:

**For Fundraising** (`.claude/fundraising.local.md`):
```yaml
---
company_name: "YourCo"
one_liner: "AI-powered analytics for SMBs"
stage: "seed"
arr: 500000
mrr_growth: 15
raise_amount: 3000000
target_valuation: 15000000
---
```

**For Board Prep & Investor Updates** (`.claude/board-prep.local.md`):
```yaml
---
company_name: "YourCo"
stage: "Series A"
industry: "B2B SaaS"
metrics:
  arr: "$2.4M"
  mrr: "$200K"
  mrr_growth: "8%"
  burn_rate: "$150K/month"
  runway: "18 months"
---
```

See each plugin's `examples/` folder for complete configuration templates.

### 4. Start using

```bash
# Generate a pitch deck outline
/pitch-deck sequoia seed

# Create investor outreach email
/outreach cold

# Analyze a term sheet
/term-sheet analyze

# Start a full board prep workflow
/board-prep:start

# Draft a monthly investor update
/investor-updates:draft
```

## Support

For issues with:
- **Claude Code plugin system**: See https://github.com/anthropics/claude-code/issues
- **These plugins**: Report at https://github.com/yamz8/open-ceo/issues

## License

MIT
