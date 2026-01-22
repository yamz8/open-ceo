---
# Board Prep Plugin Configuration
# Copy this file to .claude/board-prep.local.md in your project

company_name: Acme Corp
stage: Series A
founded: 2022

# Board composition
board_members:
  - name: Jane Smith
    role: Lead Investor
    firm: Sequoia Capital
    focus_areas:
      - growth metrics
      - go-to-market strategy
  - name: John Doe
    role: Independent Director
    background: Former CTO at BigCo
    focus_areas:
      - product roadmap
      - technical architecture
  - name: Sarah Johnson
    role: Founder/CEO
    voting: true
  - name: Mike Chen
    role: Founder/CTO
    voting: true

# Meeting cadence
meeting_cadence: quarterly
typical_duration_hours: 2
next_meeting: 2024-03-15

# Fiscal calendar
fiscal_year_end: December

# Key metrics to track
metrics:
  revenue:
    - ARR
    - MRR
    - MRR Growth Rate
  unit_economics:
    - CAC
    - LTV
    - LTV:CAC Ratio
    - Payback Period
  retention:
    - Gross Churn
    - Net Churn
    - NRR
  cash:
    - Burn Rate
    - Runway
    - Cash Balance

# Data sources (optional - helps Claude find metrics)
data_sources:
  financials: spreadsheets/financials.xlsx
  metrics_dashboard: https://app.example.com/metrics
  previous_decks: docs/board-decks/

# Standard deck sections
deck_sections:
  - executive_summary
  - metrics_dashboard
  - business_update
  - financial_review
  - go_to_market
  - product_engineering
  - team_org
  - strategic_discussion
  - board_asks
  - appendix

# Recurring strategic topics
strategic_topics:
  - Series B readiness
  - International expansion
  - Enterprise go-to-market

# Board preferences
preferences:
  send_materials_days_before: 2
  preferred_format: markdown
  include_appendix: true
---

## Company Context

Acme Corp is a B2B SaaS company providing [brief description of product/service].

### Current Priorities
1. Reach $3M ARR by end of year
2. Reduce churn to <2% monthly
3. Build enterprise sales motion

### Recent Milestones
- Closed Series A ($10M) in Q1 2023
- Launched v2.0 platform in Q3 2023
- Reached 100 customers in Q4 2023

## Board Meeting Notes

### Recurring Questions from Board
- Jane typically asks about growth efficiency (CAC payback, burn multiple)
- John focuses on product roadmap alignment with customer feedback
- Always prepare runway scenarios

### Previous Meeting Follow-ups
- [Track action items from past meetings here]

## Metrics History

### Q4 2023 Snapshot
- ARR: $2.4M
- MRR Growth: 12% MoM
- Gross Churn: 2.1%
- NRR: 115%
- Runway: 16 months

### Q3 2023 Snapshot
- ARR: $1.8M
- MRR Growth: 10% MoM
- Gross Churn: 2.8%
- NRR: 108%
- Runway: 14 months
