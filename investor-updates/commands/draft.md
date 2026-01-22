---
description: Draft a monthly investor update email
argument-hint: [format: email|markdown]
allowed-tools: Read, Write, Edit, AskUserQuestion, Glob
---

Draft a professional monthly investor update for a VC-backed startup.

## Format Options

If format argument is provided ($1):
- `email` - Generate a complete, ready-to-send email
- `markdown` - Generate a markdown draft for refinement

If no format specified, ask the user which format they prefer.

## Context Gathering

1. Check for company configuration in this order (use first one found):
   - `.claude/investor-updates.local.md` (plugin's own config)
   - `.claude/board-prep.local.md` (if using board-prep plugin)
   - `.claude/metrics.local.md` (if using metrics plugin)

2. If configuration exists, read it to get:
   - Company name and stage
   - Investor/board member list
   - Key metrics to track
   - Previous update context

3. If no configuration exists or key info missing, ask for:
   - Company name
   - Current month/period for the update
   - Key highlights (wins, milestones)
   - Current metrics (ARR/MRR, growth, runway)
   - Any challenges to mention
   - Specific asks from investors

## Update Structure

Generate the update following this structure:

### Subject Line
`[Company Name] Monthly Update - [Month Year]`

### Email Body

**1. TL;DR (2-3 bullets)**
- Lead with the most important news
- Include key metric movement
- Any critical asks

**2. Highlights**
- Major wins and milestones
- Key deals closed
- Product launches or updates
- Team additions

**3. Metrics Snapshot**
Keep it light - focus on:
- ARR/MRR and growth rate
- One key operational metric
- Runway update (if changed significantly)

**4. Challenges & Learnings**
- Be transparent but concise
- Frame challenges with what you're doing about them

**5. Asks**
- Specific, actionable requests
- Introductions needed
- Advice sought

**6. Looking Ahead**
- 1-2 priorities for next month
- Upcoming milestones

## Tone Guidelines

- Conversational but professional
- Confident but not boastful
- Transparent about challenges
- Specific with data, not vague
- Respect investor time (keep it scannable)

## Output

### For email format:
Generate a complete email with:
- Subject line
- Greeting
- Full body content
- Sign-off

### For markdown format:
Generate a structured markdown document with:
- Clear section headers
- Placeholders marked as `[TODO: ...]` for missing data
- Notes on what to customize

Ask user for preferred save location, default: `docs/investor-update-[month]-[year].md`

Reference the monthly-investor-updates skill for best practices and examples.
