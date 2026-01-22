# Startup CEO Marketplace for Claude Code

This marketplace provides plugins for VC-backed startup CEOs. Install these plugins to access AI-powered tools for fundraising, board meeting preparation, and investor communication directly within Claude Code.

**What's included:**
- **Commands**: Structured workflows for metrics, pitch decks, board decks, investor updates, hiring, founder productivity, and crisis management
- **Agents**: Proactive assistants that trigger automatically when working on metrics, fundraising, board prep, investor communication, hiring, founder challenges, or company crises
- **Skills**: Domain-specific knowledge for startup metrics, fundraising, board meetings, investor relations, compensation, founder wellness, and crisis communication

## The CEO Workflow

**Each plugin works standalone** - install only what you need. When used together, they can optionally share configuration:

```
┌─────────┐  ┌─────────────┐  ┌────────────┐  ┌──────────────────┐  ┌────────┐  ┌──────────────┐  ┌──────────────────┐
│ Metrics │  │ Fundraising │  │ Board Prep │  │ Investor Updates │  │ Hiring │  │ Founder Mode │  │ Crisis Playbook  │
└────┬────┘  └──────┬──────┘  └─────┬──────┘  └────────┬─────────┘  └───┬────┘  └──────┬───────┘  └────────┬─────────┘
     │              │               │                  │                │              │                   │
     └──────────────┴───────────────┴──────────────────┴────────────────┴──────────────┴───────────────────┘
                                 Optional: share config to avoid re-entering data
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
/plugin install hiring@open-ceo
/plugin install founder-mode@open-ceo
/plugin install crisis-playbook@open-ceo
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

---

### Founder Mode
**Plugin ID**: `founder-mode@open-ceo`

Productivity and wellness toolkit for the chaotic reality of being a startup CEO. Part executive coach, part therapist, part tough-love advisor.

**Commands:**
| Command | Description |
|---------|-------------|
| `/founder-setup` | Configure founder profile and preferences |
| `/prioritize-chaos` | Triage overwhelming to-do lists |
| `/energy-audit` | Assess where energy goes vs. should go |
| `/delegate-or-die` | Framework for effective delegation |
| `/founder-therapy` | Structured reflection for hard moments |
| `/weekly-reset` | End-of-week reflection + planning ritual |
| `/decision-journal` | Log and review major decisions |
| `/stakeholder-map` | Map relationships and who needs attention |

**Features:**
- Prioritization frameworks adapted for founders
- Delegation ladder and letting-go strategies
- Energy management and sustainable pace
- Decision journaling with review
- Burnout prevention and wellness support
- Stakeholder relationship mapping

**Requirements**: None - works with any project

---

### Crisis Playbook
**Plugin ID**: `crisis-playbook@open-ceo`

Crisis management toolkit for navigating the hardest moments. Layoffs, pivots, down rounds, PR crises, and existential threats with frameworks, communication templates, and step-by-step guidance.

**Commands:**
| Command | Description |
|---------|-------------|
| `/crisis-assess` | Assess crisis severity and determine response |
| `/layoff-plan` | Plan and execute a reduction in force |
| `/pivot-decision` | Framework for deciding whether and how to pivot |
| `/down-round-prep` | Navigate raising at a lower valuation |
| `/pr-response` | Respond to PR crises and reputation threats |

**Features:**
- Crisis severity assessment and triage
- Complete layoff planning with legal considerations
- Pivot vs. persevere decision frameworks
- Down round negotiation and communication
- PR response templates and strategies
- Restructuring and turnaround playbooks
- Stakeholder communication templates

**Requirements**: None - works with any project

---

### Hiring
**Plugin ID**: `hiring@open-ceo`

Startup hiring toolkit for CEOs. Generate job descriptions, interview scorecards, offer letters, and calculate equity compensation with benchmarks by role, level, and stage.

**Commands:**
| Command | Description |
|---------|-------------|
| `/hiring-setup` | Configure company hiring preferences and equity structure |
| `/job-description [role] [level]` | Generate role-specific job descriptions |
| `/interview-scorecard [role] [stage]` | Create structured interview evaluations |
| `/offer-letter [role] [candidate]` | Draft professional offer letters |
| `/equity-calculator [role] [level]` | Calculate equity grants and value projections |

**Features:**
- Job descriptions for any role (Engineering, Product, Sales, Marketing, etc.)
- Interview scorecards with competency-based evaluation
- Offer letters with salary and equity details
- Equity calculator with vesting schedules and exit scenarios
- Compensation benchmarks by stage, level, and location tier

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
/plugin install hiring@open-ceo          # Hiring toolkit
/plugin install founder-mode@open-ceo    # Founder productivity
/plugin install crisis-playbook@open-ceo # Crisis management
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

**For Hiring** (`.claude/hiring.local.md`):
```yaml
---
company_name: "YourCo"
stage: "series-a"
total_equity_pool_percent: 15
standard_vesting_years: 4
cliff_months: 12
fmv_per_share: 0.50
salary_percentile_target: 50
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

# Generate a job description
/job-description senior software engineer

# Create interview scorecard
/interview-scorecard product-manager technical

# Calculate equity for an offer
/equity-calculator senior series-a

# Prioritize when overwhelmed
/prioritize-chaos

# Weekly reflection and planning
/weekly-reset

# Log a major decision
/decision-journal

# Assess a crisis situation
/crisis-assess

# Plan a layoff
/layoff-plan

# Evaluate a pivot
/pivot-decision
```

## Support

For issues with:
- **Claude Code plugin system**: See https://github.com/anthropics/claude-code/issues
- **These plugins**: Report at https://github.com/yamz8/open-ceo/issues

## License

MIT
