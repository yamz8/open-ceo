# Hiring Configuration Example

Copy this file to `.claude/hiring.local.md` and fill in your company details.

```markdown
---
# Company Profile
company_name: "TechFlow"
stage: "series-a"  # pre-seed, seed, series-a, series-b, series-c
location: "San Francisco"
remote_policy: "hybrid"  # remote, hybrid, in-office

# Equity Structure
total_equity_pool_percent: 15  # percentage of company
remaining_equity_pool_percent: 10  # available for future grants
standard_vesting_years: 4
cliff_months: 12
total_shares_outstanding: 10000000  # optional, for % calculations

# 409A Valuation (optional - enables value calculations)
fmv_per_share: 0.50
last_409a_date: "2025-01-15"
preferred_price_per_share: 2.50  # last round price, for context

# Salary Philosophy
salary_percentile_target: 50  # target percentile (25, 50, 75)
location_adjustment: true  # adjust for location tier

# Benefits Summary
benefits: |
  - Health/dental/vision (100% employee, 50% dependents)
  - 401k with 4% match
  - Unlimited PTO
  - $1,000 annual learning budget
  - $500 home office stipend

# Hiring Philosophy (optional - influences JD tone)
hiring_philosophy: |
  We hire for potential over credentials. We value clear communicators
  who can work autonomously. We believe diverse teams build better products.

# Team Size (optional - helps contextualize levels)
current_headcount: 25
engineering_headcount: 12
---

## Notes

### Current Hiring Priorities
- Senior Backend Engineer (urgent)
- Product Manager
- Sales Development Rep

### Compensation Bands

| Level | Salary Range | Equity Range (% of company) |
|-------|--------------|----------------------------|
| Junior | $80-100K | 0.02-0.05% |
| Mid | $100-140K | 0.05-0.15% |
| Senior | $140-180K | 0.15-0.40% |
| Staff | $180-220K | 0.25-0.50% |
| Manager | $160-200K | 0.20-0.40% |
| Director | $200-250K | 0.40-0.75% |
| VP | $250-350K | 0.50-1.00% |

### Interview Process
1. Recruiter screen (30 min)
2. Hiring manager (45 min)
3. Technical/Skills deep-dive (60 min)
4. Team fit (45 min)
5. Founder/Executive (30 min)

### Offer Approval
- Under $150K base: Hiring manager approval
- $150-200K base: VP approval
- Over $200K or >0.25% equity: CEO approval
```
