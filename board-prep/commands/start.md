---
description: Start the full board prep workflow
allowed-tools: Read, Write, Edit, Glob, Grep, AskUserQuestion
---

Initiate a comprehensive board meeting preparation workflow for a VC-backed startup.

## Step 1: Gather Company Context

Check for existing configuration at `.claude/board-prep.local.md`. If it exists, read it to get company context.

If no configuration exists or key information is missing, ask the user for:
- Company name
- Current stage (Seed, Series A, B, etc.)
- Board member names and roles
- Meeting date (if known)
- Key metrics sources (where to find revenue, user data, etc.)

## Step 2: Create Board Prep Checklist

Generate a board prep checklist based on the startup-board-prep skill guidance. Include:

### Materials to Prepare
- [ ] Board meeting agenda
- [ ] Executive summary slide
- [ ] Metrics dashboard (ARR, MRR, growth, churn, CAC, LTV, burn, runway)
- [ ] Business update on strategic priorities
- [ ] Financial review (P&L, cash, runway)
- [ ] Product & engineering update
- [ ] Go-to-market update (sales, marketing)
- [ ] Team & org update
- [ ] Strategic discussion topics (1-2 deep-dives)
- [ ] Board asks and action items
- [ ] Appendix with supporting data

### Pre-Meeting Tasks
- [ ] Review previous board deck and minutes
- [ ] Gather latest metrics and financials
- [ ] Identify key wins and challenges
- [ ] Prepare for anticipated questions
- [ ] Send materials 48 hours in advance

## Step 3: Offer Next Steps

Ask the user which component they want to work on first:
1. Create board meeting agenda (`/board-prep:agenda`)
2. Draft board deck sections (`/board-prep:deck`)
3. Prepare for tough questions (`/board-prep:qa-prep`)
4. Update company configuration

Provide guidance based on timeline:
- If meeting is 2+ weeks away: Start with agenda and deck structure
- If meeting is 1-2 weeks away: Focus on metrics and key content
- If meeting is <1 week: Prioritize must-have sections and Q&A prep

Use the startup-board-prep skill for best practices throughout this workflow.
