---
description: Generate a professional offer letter with compensation, equity, and benefits details
argument-hint: [role] [candidate-name]
allowed-tools: Read, Grep, Glob
---

Generate an offer letter for a candidate.

**Arguments:**
- Role: $1 (e.g., "senior software engineer")
- Candidate name: $2 (optional, can prompt for it)

**Process:**

1. **Load company context:**
   - Check `.claude/hiring.local.md` for company info, benefits, equity details
   - If no config, ask for: company name, benefits summary, and equity/vesting terms

2. **Gather offer details:**
   Ask the user for:
   - Candidate's full name
   - Role title
   - Start date (or "to be determined")
   - Base salary (annual)
   - Equity grant:
     - Either number of options OR percentage of company
     - If config has 409A data, can calculate both
   - Signing bonus (if any)
   - Any other special terms

3. **Generate offer letter with sections:**

   **Header:**
   - Company letterhead placeholder
   - Date
   - Candidate name and address placeholder

   **Opening:**
   - Express excitement about extending offer
   - Confirm role title and reporting structure

   **Compensation:**
   - Base salary (annual, paid semi-monthly/bi-weekly)
   - Signing bonus (if applicable, with any clawback terms)
   - Annual bonus target (if applicable)

   **Equity:**
   - Number of stock options
   - As percentage of company (if calculable)
   - Vesting schedule (e.g., 4-year, 1-year cliff)
   - Strike price (if 409A available) or "to be determined by board"
   - Brief explanation of what options mean

   **Benefits:**
   - Health/dental/vision
   - 401k
   - PTO policy
   - Other perks from config

   **Employment Terms:**
   - At-will statement (one sentence)
   - Full-time status
   - Start date
   - Location/remote expectations
   - Note about background check if applicable

   **Closing:**
   - Offer expiration date (typically 5-7 business days)
   - Enthusiasm about them joining
   - Signature lines

   **Legal Notice:**
   - Brief statement that this is not a contract
   - Reference to employment agreement and equity docs to follow
   - Recommendation to consult legal/financial advisors

4. **Add important disclaimers:**
   - Include note at end: "This offer letter template should be reviewed by your legal counsel before sending to candidates."
   - Note that formal stock option agreement will be a separate document

**Output format:**

```markdown
# Offer Letter

[Company Name]
[Company Address]

[Date]

[Candidate Name]
[Address - to be filled]

Dear [First Name],

We are thrilled to offer you the position of **[Role Title]** at [Company Name]! We were impressed by [brief personalized note], and we're excited about what you'll bring to our team.

## Position Details

- **Title:** [Role Title]
- **Reporting to:** [Manager Name/Title]
- **Start Date:** [Date]
- **Location:** [Office location / Remote / Hybrid]

## Compensation

### Base Salary
Your annual base salary will be **$[XXX,XXX]**, paid [semi-monthly/bi-weekly] in accordance with the company's standard payroll schedule.

### Signing Bonus
[If applicable: You will receive a signing bonus of $[X,XXX], payable within 30 days of your start date. This bonus is subject to repayment if you voluntarily leave the company within 12 months.]

### Equity
You will be granted an option to purchase **[X,XXX] shares** of [Company Name] common stock[, representing approximately X.XX% of the company on a fully-diluted basis]. This grant is subject to board approval and the terms of our equity incentive plan.

- **Vesting Schedule:** [4] years with a [1]-year cliff
- **Strike Price:** [$X.XX per share / To be determined by the board based on fair market value]

The equity grant will be documented in a separate Stock Option Agreement, which will contain the complete terms and conditions.

## Benefits

As a full-time employee, you will be eligible for our benefits package, including:

- [Health/dental/vision coverage]
- [401k details]
- [PTO policy]
- [Other benefits]

Full details will be provided during onboarding.

## Employment Relationship

Your employment with [Company Name] will be "at-will," meaning either you or the company may end the employment relationship at any time, with or without cause or notice.

[If applicable: This offer is contingent upon successful completion of a background check.]

## Acceptance

This offer is valid until **[Expiration Date]**. To accept, please sign below and return this letter to [HR contact/email].

We're genuinely excited about the possibility of you joining [Company Name] and believe you'll make a significant impact on our team and mission.

Welcome aboard!

Sincerely,

___________________________
[Hiring Manager/CEO Name]
[Title]

---

**ACCEPTED AND AGREED:**

___________________________
[Candidate Name]

Date: _______________

---

*This offer letter is intended to summarize the terms of your employment and is not an employment contract. Your employment relationship will be governed by company policies and applicable law. We recommend consulting with your own legal and financial advisors regarding this offer and any equity grants.*
```

**After generating:**
Remind the user:
1. Have legal counsel review before sending
2. Prepare the formal stock option agreement separately
3. Have HR/onboarding materials ready for acceptance
