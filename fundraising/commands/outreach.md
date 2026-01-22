---
description: Create investor outreach emails (cold, warm intro, follow-up)
argument-hint: [type] [investor-name]
allowed-tools: Read, Write, Grep, Glob
---

Create investor outreach emails for fundraising.

**Arguments:**
- Type: $1 (options: cold, warm, follow-up, decline-response, or leave blank to choose)
- Investor name: $2 (optional, for personalization)

**Process:**

1. **Gather company context:**
   - Check `.claude/fundraising.local.md` for company details
   - If missing, ask for: company name, one-liner, stage, 2-3 key metrics, raise amount

2. **For cold emails:**
   - Ask which approach to use:
     - Metric-led (best when you have strong traction)
     - Story-led (best for pre-traction or unique insight)
     - Thesis-led (when investor has published relevant thesis)
   - If investor name provided, suggest personalization angles:
     - Relevant portfolio companies
     - Published content/thesis alignment
     - Mutual connections

3. **For warm intro requests:**
   - Generate the request email to the connector
   - Include a forwardable blurb for the connector
   - Coach on what makes a good intro request

4. **For follow-ups:**
   - Ask which follow-up in the sequence (1st, 2nd, 3rd/final)
   - Generate appropriate follow-up with new information angle
   - Include guidance on timing between follow-ups

5. **For decline responses:**
   - Generate graceful response that:
     - Thanks the investor
     - Asks for feedback (optional)
     - Keeps door open for future
     - Requests other introductions

**Output:**
Generate the complete email(s) with:
- Subject line
- Full email body
- Notes on personalization
- Sending tips (time of day, day of week)

**Email requirements:**
- Subject line under 50 characters
- Body under 150 words
- Clear, specific ask
- Mobile-friendly formatting
- No attachments mentioned (send deck separately if requested)
