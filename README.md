# Startup CEO Marketplace for Claude Code

This marketplace provides plugins for VC-backed startup CEOs. Install these plugins to access AI-powered tools for board meeting preparation and investor communication directly within Claude Code.

**What's included:**
- **Commands**: Structured workflows for creating board decks, agendas, and investor updates
- **Agents**: Proactive assistants that trigger automatically when working on board prep or investor communication
- **Skills**: Domain-specific knowledge for startup board meetings and investor relations

## Quick Start

```bash
# Add the marketplace
/plugin marketplace add yamz8/open-ceo

# Install plugins
/plugin install board-prep@open-ceo
/plugin install investor-updates@open-ceo
```

After installation, configure your company context (see Configuration section below).

## Available Plugins

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
/plugin install board-prep@open-ceo
/plugin install investor-updates@open-ceo
```

### 3. Configure company context

Create a `.claude/board-prep.local.md` file in your project with your company details:

```yaml
---
company_name: "YourCo"
stage: "Series A"
industry: "B2B SaaS"
fiscal_year_end: "December"
board_members:
  - name: "Investor Name"
    firm: "VC Firm"
    role: "Board Member"
metrics:
  arr: "$2.4M"
  mrr: "$200K"
  mrr_growth: "8%"
  net_revenue_retention: "115%"
  gross_margin: "78%"
  burn_rate: "$150K/month"
  runway: "18 months"
---

Additional context about your company, recent milestones, or strategic priorities.
```

Both plugins share this configuration for consistent context across board prep and investor updates.

### 4. Start using

```bash
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
