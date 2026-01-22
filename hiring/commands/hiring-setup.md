---
description: Configure company hiring preferences, equity structure, and compensation philosophy
allowed-tools: Read, Write, Edit, Grep, Glob
---

Set up hiring configuration for the company.

**Process:**

1. **Check for existing config:**
   - Look for `.claude/hiring.local.md`
   - If exists, offer to update specific sections or start fresh

2. **Gather company profile:**
   - Company name
   - Stage (pre-seed, seed, series-a, series-b, series-c)
   - Location (primary office or HQ)
   - Remote policy (remote, hybrid, in-office)
   - Current headcount (total and by department if available)

3. **Gather equity structure:**
   - Total equity pool (% of company, typically 10-20%)
   - Remaining equity pool available for future grants
   - Standard vesting schedule (typically 4 years with 1-year cliff)
   - Total shares outstanding (optional, enables % calculations)

4. **Gather 409A valuation (optional but recommended):**
   - Current FMV per share
   - Date of last 409A
   - Preferred price per share from last round (for context)

   If user doesn't have 409A yet (common for pre-seed/seed), note this and explain grants will be calculated as percentages only.

5. **Gather compensation philosophy:**
   - Target salary percentile (25th, 50th, 75th)
   - Whether to adjust for location
   - Benefits summary (health, 401k, PTO, perks)

6. **Gather hiring philosophy (optional):**
   - What the company values in candidates
   - Interview process overview
   - Any specific notes for JDs or offers

7. **Create `.claude/hiring.local.md`:**
   - Write the config file with all gathered information
   - Use YAML frontmatter for structured data
   - Include markdown notes section for freeform content

**Output format:**

```markdown
---
# Company Profile
company_name: "[Name]"
stage: "[stage]"
location: "[Location]"
remote_policy: "[policy]"

# Equity Structure
total_equity_pool_percent: [X]
remaining_equity_pool_percent: [X]
standard_vesting_years: 4
cliff_months: 12
total_shares_outstanding: [X]  # optional

# 409A Valuation (optional)
fmv_per_share: [X.XX]
last_409a_date: "[YYYY-MM-DD]"
preferred_price_per_share: [X.XX]

# Salary Philosophy
salary_percentile_target: [25/50/75]
location_adjustment: [true/false]

# Benefits Summary
benefits: |
  - [Benefit 1]
  - [Benefit 2]
  ...

# Hiring Philosophy (optional)
hiring_philosophy: |
  [Freeform notes]

# Team Size
current_headcount: [X]
---

## Notes

[Any additional notes about compensation bands, approval processes, etc.]
```

**Integration note:**
This config file can optionally read company stage from `.claude/metrics.local.md` if available, to maintain consistency across plugins.
