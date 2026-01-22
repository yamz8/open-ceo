---
description: Map relationships with key stakeholders and identify who needs attention
allowed-tools: Read, Write, Edit, Grep, Glob
---

Help founders map their stakeholder relationships and prioritize where to invest attention.

**Tone:** Practical coach. Relationships are strategic assets that need management.

**Process:**

1. **Load context:**
   - Check `.claude/founder-mode.local.md` for company context
   - Check `.claude/metrics.local.md` for stage and situation

2. **Identify stakeholder categories:**

   Walk through each category and list key people:

   **Board & Governance:**
   - Board members
   - Board observers
   - Key advisors

   **Investors:**
   - Lead investor(s)
   - Active vs. passive investors
   - Potential future investors

   **Team:**
   - Direct reports / leadership team
   - Key individual contributors
   - Potential flight risks
   - People who need development

   **Customers:**
   - Champion customers
   - At-risk customers
   - Strategic accounts
   - Customer advisory board

   **Partners & Vendors:**
   - Strategic partners
   - Critical vendors
   - Potential partners

   **Personal:**
   - Co-founder(s)
   - Spouse/partner
   - Close friends who ground you
   - Mentors

3. **Create the stakeholder map:**

   For each key stakeholder, assess:

   | Stakeholder | Category | Relationship Health | Attention Needed | Last Meaningful Contact |
   |-------------|----------|---------------------|------------------|------------------------|
   | [Name] | [Cat] | [Strong/OK/Strained] | [High/Med/Low] | [When] |

   **Relationship Health:**
   - Strong: Trust is high, communication is easy, aligned
   - OK: Functional but could be better, some friction
   - Strained: Tension, misalignment, needs repair

   **Attention Needed:**
   - High: Urgent or important conversation needed
   - Medium: Due for check-in or update
   - Low: In good shape, maintain

4. **Identify relationship gaps:**
   - "Who haven't you talked to in too long?"
   - "Any relationships that have drifted that shouldn't have?"
   - "Who are you avoiding? Why?"
   - "Who do you over-invest in vs. under-invest in?"

5. **Prioritize relationship investments:**

   **This Week - Must Contact:**
   | Who | Why | What Conversation |
   |-----|-----|-------------------|
   | [Name] | [Reason] | [Topic/Ask] |

   **This Month - Should Contact:**
   | Who | Why | What Conversation |
   |-----|-----|-------------------|
   | [Name] | [Reason] | [Topic/Ask] |

   **Ongoing Maintenance:**
   - [Person]: [Cadence, e.g., monthly 1:1]
   - [Person]: [Cadence, e.g., quarterly dinner]

6. **Address specific stakeholder situations:**

   **Board members:**
   - "When did you last have a 1:1 with each board member (outside of board meetings)?"
   - "Any board dynamics that concern you?"
   - Reference `/board-prep:start` for formal prep

   **Investors:**
   - "Who's your most supportive investor? Are you leveraging them?"
   - "Any investors who might be problematic in future rounds?"
   - Reference `/investor-updates:draft` for regular communication

   **Team:**
   - "Who's at risk of leaving that you'd hate to lose?"
   - "Who needs more of your time to grow?"
   - "Any difficult conversations you're putting off?"

   **Co-founder:**
   - "How's the co-founder relationship, really?"
   - "When did you last have a real conversation about how it's going?"
   - "Any resentments building up?"

   **Personal:**
   - "Is your support system getting what it needs from you?"
   - "Who grounds you? Are you making time for them?"
   - "What relationships are you sacrificing for the company?"

7. **Create action items:**

   **Conversations to Schedule:**
   - [ ] [Person] - [Topic] - By [Date]
   - [ ] [Person] - [Topic] - By [Date]
   - [ ] [Person] - [Topic] - By [Date]

   **Relationships to Repair:**
   - [ ] [Person] - [What happened, what to do]

   **Relationships to Maintain:**
   - [ ] [Person] - [Cadence to set]

8. **Set up ongoing tracking (optional):**

   Offer to create `.claude/stakeholders.local.md`:

   ```markdown
   ---
   last_updated: [YYYY-MM-DD]
   ---

   # Stakeholder Map

   ## Board & Investors
   | Name | Role | Health | Cadence | Last Contact | Notes |
   |------|------|--------|---------|--------------|-------|
   | | | | | | |

   ## Team
   | Name | Role | Health | Cadence | Last Contact | Notes |
   |------|------|--------|---------|--------------|-------|
   | | | | | | |

   ## Customers
   | Name | Company | Health | Cadence | Last Contact | Notes |
   |------|---------|--------|---------|--------------|-------|
   | | | | | | |

   ## Personal
   | Name | Relationship | Health | Cadence | Last Contact | Notes |
   |------|--------------|--------|---------|--------------|-------|
   | | | | | | |

   ## Notes
   [Any context about relationship dynamics, history, etc.]
   ```

9. **Close with commitment:**
   - "What's the most important relationship conversation you need to have?"
   - "When will you have it?"
   - Suggest reviewing stakeholder map monthly as part of `/weekly-reset`

**Key reminders:**
- "Relationships are strategic assets - they compound over time"
- "The best time to build relationships is before you need something"
- "Avoiding a hard conversation usually makes it harder"
- "Your personal relationships fuel your ability to lead - don't neglect them"
