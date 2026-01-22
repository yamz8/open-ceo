# Investor Updates Configuration Example

Copy this file to `.claude/investor-updates.local.md` and fill in your details.

```markdown
---
# Company Information
company_name: "Acme Corp"
stage: "Series A"

# Investor List (for recipient suggestions)
investors:
  - name: "Jane Smith"
    firm: "Acme Ventures"
    email: "jane@acmeventures.com"
    role: "Lead Investor"
  - name: "John Doe"
    firm: "Beta Capital"
    email: "john@betacap.com"
    role: "Board Member"
  - name: "Sarah Chen"
    firm: "Angel"
    email: "sarah@email.com"
    role: "Angel Investor"

# Current Metrics (update monthly)
metrics:
  arr: "$2.4M"
  mrr: "$200K"
  mrr_growth: "12%"
  runway: "18 months"
  customers: 95

# Update Preferences
preferences:
  format: "email"  # email or markdown
  send_day: "first Monday"  # when you typically send updates
---

## Recent Context

### Last Month Highlights
- Closed largest deal ever ($150K ACV)
- Launched self-serve tier
- Hired VP of Sales

### Ongoing Initiatives
- Enterprise expansion
- International planning (UK)

### Standing Asks
- Intros to Fortune 500 IT leaders
- Senior engineer referrals
```

---

## Note on Integration

This plugin works completely standalone. However, if you're also using other Open CEO plugins, you don't need to duplicate data:

- **Using metrics plugin?** The investor-updates plugin can read from `.claude/metrics.local.md`
- **Using board-prep plugin?** It can also read from `.claude/board-prep.local.md`

The plugin checks for configs in this order and uses the first one found:
1. `.claude/investor-updates.local.md`
2. `.claude/metrics.local.md`
3. `.claude/board-prep.local.md`

If none exist, the plugin simply asks for the information it needs.
