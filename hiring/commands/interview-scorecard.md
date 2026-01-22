---
description: Create a structured interview scorecard for a specific role and interview stage
argument-hint: [role] [stage]
allowed-tools: Read, Grep, Glob
---

Create an interview scorecard for evaluating candidates.

**Arguments:**
- Role: $1 (e.g., "software engineer", "product manager", "sales")
- Stage: $2 (options: phone-screen, hiring-manager, technical, team-fit, executive, or leave blank to generate for all stages)

**Interview Stages:**
- **phone-screen:** Initial qualification, culture fit, logistics (30 min)
- **hiring-manager:** Role fit, experience deep-dive, working style (45 min)
- **technical:** Skills assessment, problem-solving, domain expertise (60 min)
- **team-fit:** Collaboration, communication, values alignment (45 min)
- **executive:** Vision alignment, final assessment, selling the role (30 min)

**Process:**

1. **Load context:**
   - Check `.claude/hiring.local.md` for company values and interview process
   - If no config, ask for company name and any specific competencies to assess

2. **Determine scope:**
   - If stage specified ($2), create scorecard for that stage only
   - If no stage specified, offer to create all 5 or ask which stages they use

3. **Generate scorecard with:**

   **Header:**
   - Role being interviewed for
   - Interview stage
   - Suggested duration
   - Interviewer name (blank to fill)
   - Candidate name (blank to fill)
   - Date (blank to fill)

   **Competencies to Assess:** (4-6 per stage)
   - Role-specific competencies appropriate for this stage
   - Each with 1-2 sentence definition

   **Suggested Questions:** (2-3 per competency)
   - Behavioral questions (past experience)
   - Situational questions (hypothetical scenarios)
   - Follow-up probes

   **Rating Scale:**
   - 1 = Does not meet expectations
   - 2 = Partially meets expectations
   - 3 = Meets expectations
   - 4 = Exceeds expectations
   - 5 = Strongly exceeds expectations

   **Scoring Grid:**
   - Table with competency, rating (1-5), and notes column

   **Overall Assessment:**
   - Strong hire / Hire / No hire / Strong no hire
   - Key strengths observed
   - Concerns or areas to probe in next round
   - Recommendation for next steps

4. **Customize by role type:**

   **Engineering:**
   - Technical: System design, coding, debugging, architecture decisions
   - Phone screen: Technical communication, problem approach
   - Team fit: Code review style, collaboration, mentoring

   **Product:**
   - Technical: Product sense, prioritization frameworks, data usage
   - Phone screen: Communication, product intuition
   - Team fit: Cross-functional collaboration, stakeholder management

   **Sales:**
   - Technical: Discovery skills, objection handling, closing
   - Phone screen: Communication, energy, sales instincts
   - Team fit: Team selling, competitive nature, coachability

   **Design:**
   - Technical: Portfolio review, design process, critique ability
   - Phone screen: Design thinking, communication
   - Team fit: Collaboration with eng/product, feedback receptiveness

   **Operations/General:**
   - Technical: Process thinking, problem-solving, tool proficiency
   - Phone screen: Communication, organizational skills
   - Team fit: Cross-functional work, adaptability

**Output format:**

```markdown
# Interview Scorecard: [Role]
## [Stage Name] Interview

**Interviewer:** _______________
**Candidate:** _______________
**Date:** _______________
**Duration:** [X] minutes

---

## Competencies to Assess

### 1. [Competency Name]
[Definition of what you're looking for]

**Questions:**
- [Question 1]
  - Follow-up: [Probe]
- [Question 2]

---

[Repeat for each competency]

---

## Scoring

| Competency | Rating (1-5) | Notes |
|------------|--------------|-------|
| [Competency 1] | | |
| [Competency 2] | | |
| [Competency 3] | | |
| [Competency 4] | | |

**Rating Scale:**
1 = Does not meet | 2 = Partially meets | 3 = Meets | 4 = Exceeds | 5 = Strongly exceeds

---

## Overall Assessment

**Recommendation:** [ ] Strong Hire  [ ] Hire  [ ] No Hire  [ ] Strong No Hire

**Key Strengths:**
-

**Concerns/Areas to Probe:**
-

**Notes for Next Interviewer:**
-
```
