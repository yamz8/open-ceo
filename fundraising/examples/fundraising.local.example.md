# Fundraising Configuration Example

Copy this file to `.claude/fundraising.local.md` and fill in your company details.

```markdown
---
# Company Information
company_name: "Acme Corp"
one_liner: "AI-powered inventory management for SMB retailers"
stage: "seed"  # pre-seed, seed, series-a, series-b, series-c

# Current Raise
raise_amount: 3000000  # $3M
target_valuation: 15000000  # $15M pre-money
round_type: "priced"  # safe, convertible, priced

# Key Metrics (update monthly)
arr: 450000  # Annual recurring revenue
mrr: 37500  # Monthly recurring revenue
mrr_growth: 15  # MoM growth percentage
customers: 85
nrr: 115  # Net revenue retention %
burn_rate: 120000  # Monthly burn
runway_months: 18

# Team
founders:
  - name: "Alex Chen"
    role: "CEO"
    background: "Former PM at Shopify, Stanford CS"
  - name: "Jordan Lee"
    role: "CTO"
    background: "Ex-AWS, 10 years infrastructure"

# Pipeline (managed by /pipeline command)
pipeline: []
---

## Company Context

### What We Do
Acme Corp helps SMB retailers automatically manage their inventory using AI predictions. We integrate with their existing POS and e-commerce systems to prevent stockouts and reduce overstock.

### Key Differentiators
1. 10-minute setup (vs. weeks for enterprise solutions)
2. AI predictions trained on SMB-specific patterns
3. $99/mo starting price (10x cheaper than alternatives)

### Current Traction Highlights
- 85 paying customers, 90% SMB retailers
- $450K ARR, growing 15% MoM
- 115% NRR (strong expansion)
- <2% monthly churn

### Use of Funds
- 60% Engineering (ML team expansion)
- 25% Sales/Marketing (first sales hire)
- 15% Operations

### Target Investors
- Seed-stage B2B SaaS investors
- Retail/commerce focused funds
- AI/ML application investors
```
