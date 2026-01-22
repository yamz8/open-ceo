---
description: Generate a job description for any role with startup-appropriate framing
argument-hint: [role] [level]
allowed-tools: Read, Grep, Glob
---

Generate a job description for a specific role.

**Arguments:**
- Role: $1 (e.g., "software engineer", "product manager", "account executive")
- Level: $2 (optional: junior, mid, senior, staff, lead, manager, director, vp)

**Process:**

1. **Load company context:**
   - Check `.claude/hiring.local.md` for company info, stage, and hiring philosophy
   - If no config, ask for: company name, what they do, stage, and team size

2. **Clarify role details if needed:**
   - If role is ambiguous, ask clarifying questions:
     - Engineering: Frontend, backend, full-stack, mobile, infra, data?
     - Sales: SDR, AE, AM, Sales Manager?
     - Marketing: Growth, content, product marketing, demand gen?
   - If level not specified, ask or infer from context

3. **Generate job description with these sections:**

   **Title:** [Role Title] at [Company Name]

   **About [Company Name]:** (2-3 sentences)
   - What the company does
   - Stage and traction (if appropriate to share)
   - Why it's an exciting time to join

   **About the Role:** (1 paragraph)
   - What this person will own
   - Who they'll work with
   - Impact they'll have

   **What You'll Do:** (5-7 bullets)
   - Specific responsibilities
   - Focus on outcomes, not activities
   - Include scope and autonomy expectations

   **What We're Looking For:** (5-7 bullets)
   - Required skills and experience
   - Soft skills that matter for this role
   - "Nice to haves" clearly separated

   **Why Join Us:** (3-5 bullets)
   - Compensation and equity (if sharing ranges)
   - Benefits highlights
   - Growth opportunity
   - Team/culture highlights

   **Interview Process:** (optional, if defined in config)
   - Brief overview of stages

4. **Tailor for stage:**
   - **Pre-seed/Seed:** Emphasize ownership, ambiguity tolerance, builder mentality
   - **Series A:** Balance ownership with growing team, mention specific challenges
   - **Series B+:** Mention scale, process building, team leadership opportunities

5. **Avoid common mistakes:**
   - Don't require credentials that aren't actually necessary
   - Don't use gendered language
   - Don't list unrealistic combinations (e.g., "10 years React experience")
   - Keep requirements realistic for the level

**Output format:**

Output the complete job description in markdown, ready to copy to a job board or careers page.

**Example structure:**
```markdown
# [Role Title] at [Company Name]

## About [Company Name]
[Company description...]

## About the Role
[Role overview...]

## What You'll Do
- [Responsibility 1]
- [Responsibility 2]
...

## What We're Looking For
**Required:**
- [Requirement 1]
- [Requirement 2]
...

**Nice to Have:**
- [Bonus 1]
...

## Why Join Us
- [Reason 1]
- [Reason 2]
...

## How to Apply
[Application instructions or note about process]
```
