# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Open CEO is a Claude Code plugin marketplace containing 5 specialized plugins for VC-backed startup CEOs. The plugins provide AI-powered tools for: metrics tracking, fundraising, board meeting preparation, investor communication, and hiring.

**Architecture**: This is a markdown and JSON-based plugin system with no external dependencies. All business logic and knowledge lives in markdown files.

## Plugin Structure

Each plugin follows an identical modular structure:

```
plugin-name/
├── .claude-plugin/plugin.json    # Plugin manifest
├── README.md                     # Plugin documentation
├── agents/                       # Proactive assistants with trigger conditions
├── commands/                     # Slash commands with YAML frontmatter
├── skills/                       # Knowledge bases with reference docs
└── examples/                     # Config templates and sample outputs
```

**Commands**: Interactive workflows triggered by `/command-name [args]`. Each has YAML frontmatter defining description, argument hints, and allowed tools.

**Agents**: Autonomous assistants with trigger conditions, system prompts, and tool access (Read, Write, Edit, Glob, Grep).

**Skills**: Comprehensive knowledge bases with trigger conditions, examples, and reference documentation.

## Cross-Plugin Integration

Plugins are standalone but can optionally share data via `.claude/[plugin].local.md` config files:

```
Metrics (.local.md) ← Fundraising, Board Prep, Investor Updates (read metrics data)
```

Each plugin checks for its own config first, then falls back to metrics config, then asks the user.

## The Five Plugins

| Plugin | Purpose | Commands |
|--------|---------|----------|
| `metrics@open-ceo` | Track SaaS/Marketplace metrics, benchmarks | `/metrics-setup`, `/metrics-snapshot`, `/metrics-benchmark`, `/metrics-calculate` |
| `fundraising@open-ceo` | Pitch decks, outreach, term sheets, pipeline | `/pitch-deck`, `/outreach`, `/term-sheet`, `/due-diligence`, `/pipeline` |
| `board-prep@open-ceo` | Board meeting preparation workflow | `/board-prep:start`, `/board-prep:agenda`, `/board-prep:deck`, `/board-prep:qa-prep` |
| `investor-updates@open-ceo` | Monthly investor update drafting | `/investor-updates:draft`, `/investor-updates:metrics`, `/investor-updates:send-checklist` |
| `hiring@open-ceo` | Job descriptions, interviews, offers, equity | `/hiring-setup`, `/job-description`, `/interview-scorecard`, `/offer-letter`, `/equity-calculator` |

## Key Files

- `README.md` - Main marketplace guide
- `.claude-plugin/marketplace.json` - Registry of all plugins with metadata
- `*/commands/*.md` - Slash command definitions
- `*/agents/*.md` - Agent trigger conditions and system prompts
- `*/skills/*/SKILL.md` - Knowledge base entry points
- `*/examples/*.local.md` - Config file templates showing required fields

## Adding New Content

**New command**: Add `commands/[name].md` with YAML frontmatter (description, argument_hint, allowed_tools) + workflow instructions

**New agent**: Add `agents/[name].md` with trigger examples + system prompt

**New skill**: Add `skills/[name]/SKILL.md` with triggers + reference content in subdirectories

**New plugin**: Create top-level directory following existing structure, update `.claude-plugin/marketplace.json`

## Installation

```bash
# Add marketplace
/plugin marketplace add https://github.com/yamz8/open-ceo.git

# Install individual plugins
/plugin install metrics@open-ceo
```
