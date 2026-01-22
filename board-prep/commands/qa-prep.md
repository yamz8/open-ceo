---
description: Prepare for anticipated investor questions
argument-hint: [focus-area]
allowed-tools: Read, Write, AskUserQuestion
---

Prepare talking points and responses for anticipated board/investor questions.

## Focus Areas

If a specific focus area is provided ($1), concentrate on that category:
- `financial` - Runway, profitability, unit economics questions
- `growth` - Growth rate, market, competition questions
- `operations` - Churn, sales, product questions
- `team` - Hiring, retention, organization questions
- `strategic` - Strategy, pivots, market timing questions
- `all` - Comprehensive Q&A prep across all areas

## Context Gathering

1. Check for company configuration at `.claude/board-prep.local.md`
2. Ask user about current situation:
   - Any recent misses or challenges to address?
   - Hot topics from last board meeting?
   - Any metrics trending in concerning direction?
   - Recent competitive moves to discuss?
   - Upcoming decisions that may raise questions?

## Question Categories to Cover

### Financial Questions
- What's your runway and fundraising plan?
- When will you be profitable?
- Why did you miss/beat forecast?
- How are you managing burn?

### Growth Questions
- What's driving growth/slowdown?
- Who's the competition and how are you differentiated?
- What's the TAM and penetration strategy?
- Why now for this market?

### Operational Questions
- Why is churn [increasing/elevated]?
- How's the sales team performing?
- What's the biggest risk?
- How's product adoption?

### Team Questions
- Any key person risk?
- How's the team doing?
- When are you hiring [key role]?
- Any regrettable departures?

### Strategic Questions
- What would you do with more capital?
- What keeps you up at night?
- What would you do differently?
- What's the 3-year vision?

## Response Framework

For each anticipated question, prepare:

1. **Acknowledge** - Show understanding of the concern
2. **Frame** - Provide context before details
3. **Data** - Support with specific facts
4. **Action** - What's being done about it
5. **Outcome** - Expected results and timeline

## Output Format

Generate a Q&A preparation document with:
- Prioritized list of anticipated questions
- Prepared response framework for each
- Supporting data points to reference
- Red flags to address proactively

## Output Location

Ask user for preferred location, default: `docs/board-qa-prep-[date].md`

Reference the investor questions guide in the startup-board-prep skill for comprehensive question bank and response strategies.
