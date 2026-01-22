# open-ceo

A Claude Code plugin marketplace providing AI-powered tools for VC-backed startup CEOs. Automate and streamline critical investor-facing communication and board management tasks.

## Plugins

### board-prep

Comprehensive board meeting preparation toolkit.

| Command | Description |
|---------|-------------|
| `/board-prep:start` | Full board prep workflow with checklist |
| `/board-prep:agenda` | Generate professional board meeting agenda |
| `/board-prep:deck` | Draft board deck sections in markdown |
| `/board-prep:qa-prep` | Prepare for anticipated investor questions |

**Features:**
- 10-section board deck generation (summary, metrics, business updates, financials, etc.)
- SaaS metrics tracking (ARR, MRR, growth rates, churn, CAC, LTV, runway)
- Investor Q&A preparation across 5 focus areas
- Configurable agenda formats (90-min, 2-hour, 3-hour)

### investor-updates

Monthly investor communication assistant.

| Command | Description |
|---------|-------------|
| `/investor-updates:draft` | Draft monthly investor update |
| `/investor-updates:metrics` | Generate metrics snapshot |
| `/investor-updates:send-checklist` | Pre-send verification checklist |

**Features:**
- Structured update format (TL;DR, Highlights, Metrics, Challenges, Asks)
- 2-3 minute read optimization (300-500 words)
- Email or markdown output formats
- 20+ item pre-send checklist

## Installation

Add the marketplace to your Claude Code configuration:

```bash
claude plugins:add https://github.com/yamz8/open-ceo
```

Or install individual plugins:

```bash
claude plugins:add https://github.com/yamz8/open-ceo/board-prep
claude plugins:add https://github.com/yamz8/open-ceo/investor-updates
```

## Configuration

Create a `.claude/board-prep.local.md` file in your project with your company context:

```yaml
---
company_name: "YourCo"
stage: "Series A"
industry: "B2B SaaS"
board_members:
  - name: "Investor Name"
    firm: "VC Firm"
    role: "Board Member"
---
```

Both plugins share this configuration for consistent context across board prep and investor updates.

## Project Structure

```
open-ceo/
├── board-prep/              # Board meeting preparation plugin
│   ├── agents/              # Proactive AI assistants
│   ├── commands/            # User-callable commands
│   └── skills/              # Knowledge bases & templates
├── investor-updates/        # Monthly update plugin
│   ├── agents/
│   ├── commands/
│   └── skills/
└── .claude-plugin/
    └── marketplace.json     # Plugin registry
```

## License

MIT