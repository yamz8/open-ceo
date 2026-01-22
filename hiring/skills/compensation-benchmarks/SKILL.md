---
name: Compensation Benchmarks
description: This skill should be used when the user asks about "salary ranges", "equity grants", "compensation benchmarks", "how much to pay", "competitive offer", "market rate", "startup compensation", "equity percentages", "option grants", or mentions specific compensation questions like "what should I pay a senior engineer" or "how much equity for a VP".
version: 0.1.0
---

# Startup Compensation Benchmarks

## Overview

This skill provides salary and equity benchmark data for startup hiring. Data is segmented by company stage, role level, and location tier to help CEOs make competitive offers.

## How to Use This Data

1. **Identify company stage** (Seed, Series A, B, C+)
2. **Determine role level** (IC, Senior, Staff, Manager, Director, VP, C-level)
3. **Apply location tier adjustment** (Tier 1, 2, or 3)
4. **Consider percentile target** (25th for budget-conscious, 50th for competitive, 75th for aggressive)

## Salary Benchmarks by Stage and Level

### Seed Stage Companies

| Level | 25th %ile | 50th %ile | 75th %ile |
|-------|-----------|-----------|-----------|
| Junior IC | $70K | $85K | $100K |
| Mid IC | $90K | $110K | $130K |
| Senior IC | $120K | $145K | $170K |
| Staff IC | $150K | $175K | $200K |
| Manager | $130K | $155K | $180K |
| Director | $160K | $190K | $220K |
| VP | $180K | $220K | $260K |

### Series A Companies

| Level | 25th %ile | 50th %ile | 75th %ile |
|-------|-----------|-----------|-----------|
| Junior IC | $80K | $95K | $115K |
| Mid IC | $100K | $125K | $150K |
| Senior IC | $140K | $165K | $190K |
| Staff IC | $170K | $200K | $230K |
| Manager | $150K | $175K | $200K |
| Director | $180K | $215K | $250K |
| VP | $220K | $270K | $320K |

### Series B Companies

| Level | 25th %ile | 50th %ile | 75th %ile |
|-------|-----------|-----------|-----------|
| Junior IC | $90K | $105K | $125K |
| Mid IC | $115K | $140K | $165K |
| Senior IC | $155K | $185K | $215K |
| Staff IC | $190K | $225K | $260K |
| Manager | $165K | $195K | $225K |
| Director | $200K | $240K | $280K |
| VP | $260K | $310K | $360K |

### Series C+ Companies

| Level | 25th %ile | 50th %ile | 75th %ile |
|-------|-----------|-----------|-----------|
| Junior IC | $100K | $120K | $140K |
| Mid IC | $130K | $155K | $180K |
| Senior IC | $170K | $200K | $235K |
| Staff IC | $210K | $250K | $290K |
| Manager | $180K | $215K | $250K |
| Director | $225K | $270K | $315K |
| VP | $300K | $360K | $420K |

## Location Tier Adjustments

| Tier | Description | Multiplier |
|------|-------------|------------|
| Tier 1 | SF, NYC, Seattle | 1.0x (baseline) |
| Tier 2 | LA, Boston, Austin, Denver, DC | 0.90x |
| Tier 3 | Remote / Other locations | 0.80-0.85x |

**Application:** Multiply base salary by location multiplier.

## Equity Benchmarks by Stage and Level

Equity shown as percentage of fully-diluted company ownership.

### Seed Stage

| Level | 25th %ile | 50th %ile | 75th %ile |
|-------|-----------|-----------|-----------|
| Junior IC | 0.02% | 0.05% | 0.10% |
| Mid IC | 0.05% | 0.10% | 0.20% |
| Senior IC | 0.10% | 0.25% | 0.50% |
| Staff IC | 0.25% | 0.50% | 0.75% |
| Manager | 0.15% | 0.30% | 0.50% |
| Director | 0.40% | 0.75% | 1.00% |
| VP | 0.75% | 1.25% | 2.00% |

### Series A

| Level | 25th %ile | 50th %ile | 75th %ile |
|-------|-----------|-----------|-----------|
| Junior IC | 0.01% | 0.025% | 0.05% |
| Mid IC | 0.025% | 0.05% | 0.10% |
| Senior IC | 0.05% | 0.15% | 0.30% |
| Staff IC | 0.15% | 0.30% | 0.50% |
| Manager | 0.10% | 0.20% | 0.35% |
| Director | 0.25% | 0.50% | 0.75% |
| VP | 0.50% | 1.00% | 1.50% |

### Series B

| Level | 25th %ile | 50th %ile | 75th %ile |
|-------|-----------|-----------|-----------|
| Junior IC | 0.005% | 0.015% | 0.03% |
| Mid IC | 0.015% | 0.03% | 0.06% |
| Senior IC | 0.03% | 0.08% | 0.15% |
| Staff IC | 0.08% | 0.15% | 0.25% |
| Manager | 0.05% | 0.10% | 0.20% |
| Director | 0.15% | 0.30% | 0.50% |
| VP | 0.30% | 0.60% | 1.00% |

### Series C+

| Level | 25th %ile | 50th %ile | 75th %ile |
|-------|-----------|-----------|-----------|
| Junior IC | 0.002% | 0.005% | 0.01% |
| Mid IC | 0.005% | 0.015% | 0.03% |
| Senior IC | 0.015% | 0.04% | 0.08% |
| Staff IC | 0.04% | 0.08% | 0.15% |
| Manager | 0.025% | 0.05% | 0.10% |
| Director | 0.08% | 0.15% | 0.30% |
| VP | 0.15% | 0.35% | 0.60% |

## Role-Specific Adjustments

### Engineering
- Machine Learning / AI: +10-20% salary premium
- Security / Infrastructure: +5-15% salary premium
- Frontend typically at baseline

### Sales
- Base + OTE structure (typically 50/50 or 60/40 split)
- AE OTE typically 2x base
- Sales leadership may have accelerators

### Executive Hires
- C-level equity: 1-5% depending on stage and role
- CEO typically retains largest stake
- CTO/CFO often second-tier equity

## Refresh Grants

Annual equity refreshes to retain talent:

| Stage | Typical Annual Refresh |
|-------|----------------------|
| Seed | 25-50% of original grant |
| Series A | 20-40% of original grant |
| Series B | 15-30% of original grant |
| Series C+ | 10-25% of original grant |

## Total Compensation Philosophy

**Cash vs. Equity Tradeoffs:**
- Earlier stage = more equity, less cash
- Candidate with family/mortgage may prefer cash
- Experienced candidates often value equity more
- Consider candidate's risk tolerance

**Competitive Positioning:**
- 25th percentile: Budget-conscious, offset with equity or mission
- 50th percentile: Market-competitive baseline
- 75th percentile: Aggressive hiring, competing for top talent

## Additional Resources

For detailed role-specific guidance, see:
- **`references/engineering-compensation.md`** - Engineering role breakdowns
- **`references/sales-compensation.md`** - Sales comp structures
- **`references/executive-compensation.md`** - C-level and VP packages
