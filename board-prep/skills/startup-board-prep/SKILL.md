---
name: Startup Board Prep
description: This skill should be used when the user asks to "prepare for a board meeting", "create a board deck", "draft investor update", "prepare board agenda", "calculate runway", "prepare for investor questions", or mentions board meetings, investor updates, board decks, or quarterly updates for a VC-backed startup.
version: 0.1.0
---

# Startup Board Prep

Guidance for helping VC-backed startup CEOs prepare comprehensive, professional board meeting materials.

## Overview

Board meetings are critical governance events for VC-backed startups. Effective preparation requires:
- Clear agenda with time allocations
- Updated metrics and KPIs
- Structured narrative covering progress, challenges, and plans
- Preparation for tough investor questions

## Board Prep Workflow

### 1. Gather Company Context

Before creating any materials, gather essential context:

- Company name and stage (Seed, Series A, B, etc.)
- Board composition (investors, independents, founders)
- Meeting cadence (monthly, quarterly)
- Previous board materials if available
- Current metrics and data sources

Check for `.claude/board-prep.local.md` for stored company context.

### 2. Create Meeting Agenda

Standard board meeting agenda structure:

| Section | Duration | Purpose |
|---------|----------|---------|
| Opening & Administrative | 5 min | Approvals, minutes |
| CEO Update | 15-20 min | High-level narrative |
| Financial Review | 15-20 min | Metrics deep-dive |
| Strategic Discussion | 20-30 min | Key decisions, challenges |
| Closed Session | 10-15 min | Board-only discussion |

Adjust timing based on meeting length (typically 1.5-2 hours for board meetings).

### 3. Draft Board Deck

Structure the deck following the standard flow:

1. **Executive Summary** - Key highlights, asks, decisions needed
2. **Metrics Dashboard** - SaaS metrics at a glance
3. **Business Update** - Progress on OKRs/initiatives
4. **Financial Review** - P&L, burn, runway
5. **Product/Engineering** - Roadmap, releases, tech debt
6. **Go-to-Market** - Sales, marketing, customer success
7. **Team & Org** - Headcount, hiring, culture
8. **Strategic Topics** - Deep-dive on 1-2 key issues
9. **Asks & Discussion** - What you need from the board
10. **Appendix** - Detailed data, backup slides

See `references/deck-structure.md` for detailed guidance on each section.

### 4. Prepare Key Metrics

Essential SaaS metrics to include:

**Revenue Metrics:**
- ARR (Annual Recurring Revenue)
- MRR (Monthly Recurring Revenue)
- MRR Growth Rate (MoM and YoY)
- Net Revenue Retention (NRR)

**Unit Economics:**
- CAC (Customer Acquisition Cost)
- LTV (Lifetime Value)
- LTV:CAC Ratio (target: >3:1)
- Payback Period

**Retention & Churn:**
- Gross Churn Rate
- Net Churn Rate
- Logo Retention

**Cash & Runway:**
- Monthly Burn Rate
- Cash Balance
- Runway (months)

See `references/metrics-guide.md` for calculation formulas and benchmarks.

### 5. Anticipate Investor Questions

Prepare for common investor concerns:

- Runway and fundraising timeline
- Path to profitability
- Competitive threats
- Key person dependencies
- Customer concentration
- Sales pipeline and forecast accuracy

See `references/investor-questions.md` for comprehensive Q&A preparation.

## Writing Effective Board Materials

### Narrative Structure

Frame updates using the "Context → Progress → Challenges → Plan" structure:

1. **Context**: Remind board of strategic priorities
2. **Progress**: Celebrate wins with specific metrics
3. **Challenges**: Be transparent about problems
4. **Plan**: Show clear path forward

### Tone Guidelines

- Be direct and concise
- Lead with the headline (don't bury key information)
- Use data to support claims
- Acknowledge challenges proactively
- Show accountability and ownership

### Visual Best Practices

- One key message per slide
- Use charts over tables where possible
- Highlight changes from previous period
- Use consistent color coding (green=good, red=concern)
- Include trend lines, not just point-in-time data

## Common Pitfalls to Avoid

1. **Information overload** - Focus on what matters, use appendix for detail
2. **Missing the narrative** - Data without context is noise
3. **Hiding bad news** - Investors find out eventually; be proactive
4. **No clear asks** - Always have specific requests for the board
5. **Last-minute prep** - Start 2+ weeks before meeting

## Settings and Configuration

Store company-specific information in `.claude/board-prep.local.md`:

```yaml
---
company_name: Acme Corp
stage: Series A
board_members:
  - name: Jane Smith
    role: Lead Investor
    firm: Sequoia
meeting_cadence: quarterly
fiscal_year_end: December
---
```

## Additional Resources

### Reference Files

For detailed guidance, consult:
- **`references/metrics-guide.md`** - SaaS metrics definitions, formulas, and benchmarks
- **`references/deck-structure.md`** - Detailed board deck section guidance
- **`references/investor-questions.md`** - Common questions and response strategies

### Example Files

Working examples in `examples/`:
- **`examples/sample-agenda.md`** - Complete board meeting agenda template
- **`examples/sample-deck-outline.md`** - Board deck outline with section guidance
