---
description: Configure your founder profile, priorities, and personal context
allowed-tools: Read, Write, Edit, Grep, Glob
---

Set up founder mode configuration for personalized assistance.

**Process:**

1. **Check for existing config:**
   - Look for `.claude/founder-mode.local.md`
   - If exists, offer to update specific sections or start fresh
   - Also check for `.claude/metrics.local.md` to pull company context

2. **Gather company context (or import from metrics):**
   - Company name
   - Stage (pre-seed, seed, series-a, series-b+)
   - Runway (months)
   - Team size
   - Key metrics the founder tracks

3. **Gather personal context:**
   - Role (solo founder, CEO with co-founder, etc.)
   - Months since founding
   - Biggest current challenge (growth, fundraising, team, product, personal)
   - Working style preferences (early bird, night owl, etc.)

4. **Gather energy profile:**
   - When they do their best deep work
   - What tasks drain them most
   - What tasks energize them
   - Current weekly time allocation (product, team, fundraising, admin, etc.)

5. **Gather support system:**
   - Do they have a coach, therapist, or advisor?
   - Peer founder support (groups, close founder friends)
   - Family/partner situation (supportive, strained, etc.)

6. **Gather priorities and constraints:**
   - Top 3 priorities for next 90 days
   - What they've been avoiding
   - Non-negotiable personal commitments (family time, exercise, etc.)

7. **Create `.claude/founder-mode.local.md`:**
   - Write the config file with all gathered information
   - Use YAML frontmatter for structured data
   - Include markdown notes for freeform context

**Output format:**

```markdown
---
# Company Context
company_name: "[Name]"
stage: "[stage]"
runway_months: [X]
team_size: [X]

# Founder Profile
role: "[solo-founder/ceo-with-cofounder/etc]"
months_since_founding: [X]
biggest_challenge: "[growth/fundraising/team/product/personal]"

# Energy Profile
best_deep_work_time: "[early-morning/morning/afternoon/evening/night]"
energy_drainers:
  - "[task/meeting type]"
  - "[task/meeting type]"
energy_boosters:
  - "[task/activity]"
  - "[task/activity]"

# Current Time Allocation (hours/week, should sum to ~50-60)
time_allocation:
  product: [X]
  team: [X]
  fundraising: [X]
  sales: [X]
  admin: [X]
  other: [X]

# Support System
has_coach: [true/false]
has_therapist: [true/false]
founder_peers: "[none/few/strong-network]"
family_support: "[supportive/neutral/strained]"

# Current Priorities (90 days)
priorities:
  - "[Priority 1]"
  - "[Priority 2]"
  - "[Priority 3]"

# What You're Avoiding
avoiding:
  - "[Thing 1]"
  - "[Thing 2]"

# Non-Negotiables
non_negotiables:
  - "[Commitment 1]"
  - "[Commitment 2]"
---

## Notes

[Any additional context about current situation, recent events, or things the founder wants to remember]
```

**After setup:**
- Summarize their profile back to them
- Highlight any potential concerns (e.g., no support system, unsustainable hours)
- Suggest which founder-mode commands might be most relevant right now
