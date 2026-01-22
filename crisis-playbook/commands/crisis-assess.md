---
description: Assess the severity and type of crisis you're facing
argument-hint: "[optional: brief description of the situation]"
allowed-tools: Read, Write, Edit, Grep, Glob
---

Help founders assess and categorize the crisis they're facing to determine appropriate response.

**Tone:** Calm, direct, structured. Bring clarity to chaos.

**Process:**

1. **Understand the situation:**
   If they provided context, acknowledge it. Otherwise ask:
   - "What's happening? Give me the facts, not the fears."
   - "When did this start? How quickly is it evolving?"
   - "Who knows about this? Who needs to know?"

2. **Load context (if available):**
   - Check `.claude/metrics.local.md` for runway, burn, team size
   - Check `.claude/crisis-playbook.local.md` for any prior crisis context

3. **Categorize the crisis:**

   | Crisis Type | Examples | Typical Urgency |
   |-------------|----------|-----------------|
   | **Financial** | Running out of cash, failed fundraise, revenue collapse | Days to weeks |
   | **People** | Key departure, layoffs needed, co-founder conflict | Weeks |
   | **Product** | Product not working, major pivot needed | Weeks to months |
   | **Legal** | Lawsuit, regulatory issue, IP problem | Varies |
   | **Reputation** | Bad press, social media crisis, customer backlash | Hours to days |
   | **Operational** | Major outage, security breach, supply chain | Hours to days |

4. **Assess severity:**

   | Level | Description | Response Mode |
   |-------|-------------|---------------|
   | **Critical** | Existential threat, immediate action required | War room, all hands |
   | **Severe** | Major impact, needs attention this week | Focused effort, daily check-ins |
   | **Moderate** | Significant but manageable, needs a plan | Structured approach, weekly tracking |
   | **Low** | Concerning but not urgent | Monitor, address in normal course |

5. **Assess the timeline:**
   - "How long until this becomes critical if we do nothing?"
   - "What's the point of no return?"
   - "How much time do we have to make a decision?"

6. **Map the stakeholders:**
   - Who is affected?
   - Who needs to be informed?
   - Who needs to be involved in the response?
   - Who might make things worse if not handled correctly?

7. **Identify immediate actions:**

   **In the next 24 hours:**
   - [ ] What must happen immediately?
   - [ ] Who must be told?
   - [ ] What must NOT happen (things that would make it worse)?

   **In the next week:**
   - [ ] What decisions need to be made?
   - [ ] What information do we need?
   - [ ] Who do we need to involve?

8. **Create the crisis assessment:**

   ```markdown
   # Crisis Assessment
   Date: [YYYY-MM-DD]

   ## Situation Summary
   [2-3 sentence factual description]

   ## Classification
   - **Type:** [Financial/People/Product/Legal/Reputation/Operational]
   - **Severity:** [Critical/Severe/Moderate/Low]
   - **Timeline:** [How long until critical]

   ## Key Facts
   - [Fact 1]
   - [Fact 2]
   - [Fact 3]

   ## Unknown/Uncertain
   - [What we don't know yet]

   ## Stakeholders
   | Who | Impact | Need to Inform? | Need to Involve? |
   |-----|--------|-----------------|------------------|
   | | | | |

   ## Immediate Actions (24h)
   - [ ] [Action 1]
   - [ ] [Action 2]

   ## This Week
   - [ ] [Action 1]
   - [ ] [Action 2]

   ## Decisions Needed
   - [Decision 1] - By [date]
   - [Decision 2] - By [date]

   ## Next Command
   Based on this crisis, the next step is: [/layoff-plan, /pivot-decision, /down-round-prep, /pr-response, or other]
   ```

9. **Recommend next steps:**
   Based on the crisis type, point them to the right command:
   - Layoffs needed → `/layoff-plan`
   - Pivot consideration → `/pivot-decision`
   - Fundraising crisis → `/down-round-prep`
   - PR/reputation → `/pr-response`
   - Other → Provide custom guidance

10. **Close with grounding:**
    - "This is hard, but you can handle it."
    - "Most companies face crises. It's how you respond that matters."
    - "What support do you need right now?"

**Key reminders:**
- In a crisis, clarity is the first step
- Don't let fear drive decisions - let facts drive them
- Speed matters, but so does not making things worse
- You're not alone - involve the right people
