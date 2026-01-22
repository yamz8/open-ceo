# Startup CEO Marketplace for Claude Code

This marketplace provides plugins for VC-backed startup CEOs. Install these plugins to access AI-powered tools for fundraising, board meeting preparation, and investor communication directly within Claude Code.

**What's included:**
- **Commands**: Structured workflows for metrics, pitch decks, board decks, and investor updates
- **Agents**: Proactive assistants that trigger automatically when working on metrics, fundraising, board prep, or investor communication
- **Skills**: Domain-specific knowledge for startup metrics, fundraising, board meetings, and investor relations

## The CEO Workflow

**Each plugin works standalone** - install only what you need. When used together, they can optionally share configuration:

```
   ┌─────────────┐  ┌────────────┐  ┌──────────────────┐  ┌──────────────────┐
   │   Metrics   │  │ Fundraising │  │   Board Prep    │  │ Investor Updates │
   │ (standalone)│  │ (standalone)│  │   (standalone)  │  │   (standalone)   │
   └──────┬──────┘  └──────┬──────┘  └────────┬────────┘  └────────┬─────────┘
          │                │                   │                    │
          └────────────────┴───────────────────┴────────────────────┘
                              Optional: Share config to avoid re-entering data
```

## Quick Start

```bash
# Add the marketplace
/plugin marketplace add yamz8/open-ceo

# Install only what you need (each plugin works standalone)
/plugin install metrics@open-ceo
/plugin install fundraising@open-ceo
/plugin install board-prep@open-ceo
/plugin install investor-updates@open-ceo
```

**No configuration required** - each plugin will ask for information when needed. Optional config files can save time if you use plugins frequently.

## Available Plugins

### Metrics
**Plugin ID**: `metrics@open-ceo`

Track, calculate, and benchmark startup metrics. Works standalone or as optional shared config for other plugins.

**Commands:**
| Command | Description |
|---------|-------------|
| `/metrics-setup [model] [stage]` | Configure metrics tracking |
| `/metrics-snapshot [format]` | Generate metrics report |
| `/metrics-benchmark [stage]` | Compare to industry benchmarks |
| `/metrics-calculate [metric]` | Calculate derived metrics |

**Features:**
- SaaS metrics (ARR, MRR, NRR, churn, CAC, LTV, burn multiple, etc.)
- Marketplace metrics (GMV, take rate, liquidity, network effects)
- Stage-appropriate benchmarks (pre-seed to Series C)
- Optional: Other plugins can read your metrics config

**Requirements**: None - works standalone with any project

---

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
# Install only what you need - each works standalone
/plugin install metrics@open-ceo         # Metrics tracking
/plugin install fundraising@open-ceo     # Fundraising toolkit
/plugin install board-prep@open-ceo      # Board meeting prep
/plugin install investor-updates@open-ceo # Monthly updates
```

### 3. Configure company context (optional)

**Configuration is optional** - each plugin will ask for information when needed.

For convenience, you can create config files to avoid re-entering information:

**For Metrics** (`.claude/metrics.local.md`):
```yaml
---
company_name: "YourCo"
business_model: "saas"
stage: "series-a"
mrr: 185000
nrr: 112
gross_margin: 78
burn_multiple: 1.8
---
```

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

**For Board Prep** (`.claude/board-prep.local.md`):
```yaml
---
company_name: "YourCo"
stage: "Series A"
board_members:
  - name: "Jane Smith"
    firm: "Acme Ventures"
---
```

**For Investor Updates** (`.claude/investor-updates.local.md`):
```yaml
---
company_name: "YourCo"
stage: "Series A"
investors:
  - name: "Jane Smith"
    firm: "Acme Ventures"
---
```

See each plugin's `examples/` folder for complete templates.

**Note**: If you have multiple plugins, they can optionally read each other's configs - you don't need to duplicate information. Each plugin checks for configs in a fallback order.

### 4. Start using

```bash
# Set up metrics tracking
/metrics-setup saas series-a

# Generate a metrics snapshot
/metrics-snapshot

# Benchmark your metrics
/metrics-benchmark

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
