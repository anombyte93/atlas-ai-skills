# Atlas AI Skills

[![Claude Code Plugin](https://img.shields.io/badge/Claude_Code-Plugin-8A2BE2)](https://github.com/anombyte93/atlas-ai-skills)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/anombyte93/atlas-ai-skills/blob/main/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/anombyte93/atlas-ai-skills)](https://github.com/anombyte93/atlas-ai-skills/stargazers)

Production AI development toolkit for Claude Code. Five skills, one install.

## Install

### As Plugin (Recommended)

```bash
claude plugin add /path/to/atlas-ai-skills
```

Or clone and reference:

```bash
git clone https://github.com/anombyte93/atlas-ai-skills.git ~/.claude/plugins/atlas-ai-skills
```

### Individual Skills

Each skill can also be installed standalone from its own repo:

| Skill | Command | Repo |
|-------|---------|------|
| `/prd` | `curl -fsSL https://raw.githubusercontent.com/anombyte93/prd-taskmaster/master/install.sh \| bash` | [prd-taskmaster](https://github.com/anombyte93/prd-taskmaster) |
| `/start` | `curl -fsSL https://raw.githubusercontent.com/anombyte93/claude-session-init/main/install.sh \| bash` | [claude-session-init](https://github.com/anombyte93/claude-session-init) |
| `/codify` | `curl -fsSL https://raw.githubusercontent.com/anombyte93/codify/main/install.sh \| bash` | [codify](https://github.com/anombyte93/codify) |
| `/research-before-coding` | `curl -fsSL https://raw.githubusercontent.com/anombyte93/claude-research-skill/main/install.sh \| bash` | [claude-research-skill](https://github.com/anombyte93/claude-research-skill) |
| `/accomplish` | `curl -fsSL https://raw.githubusercontent.com/anombyte93/claude-accomplish-skill/main/install.sh \| bash` | [claude-accomplish-skill](https://github.com/anombyte93/claude-accomplish-skill) |

## What's Included

### `/prd` — PRD Generator + TaskMaster (94 stars)
Generate comprehensive Product Requirements Documents optimized for AI-assisted task breakdown. 13 automated quality checks, autonomous execution modes, datetime tracking.

### `/start` — Session Memory (75 stars)
Persistent project memory across Claude Code sessions. Bootstraps structured context, organizes files, manages soul purpose lifecycle with completion verification.

### `/codify` — Skill Optimizer
Extract deterministic operations from any Claude Code skill into a Python script. Reduces SKILL.md by 60-80% while preserving all AI judgment.

### `/research-before-coding` — Research Enforcer
Mandatory research via Perplexity before any implementation code. Delegates to fast subagent, returns distilled summaries. No guessing.

### `/accomplish` — Daily Journal
Log rich accomplishments with AI-crafted reflections. Timestamps, git context, and session mirroring.

## Architecture

Each skill follows the **codification pattern**: deterministic operations in `script.py`, AI judgment in `SKILL.md`.

```
skills/
├── prd-taskmaster/     SKILL.md + script.py (11 subcommands) + templates/
├── start/              SKILL.md + session-init.py (9 subcommands)
├── codify/             SKILL.md (pure judgment — codifies other skills)
├── research-before-coding/  SKILL.md + query-patterns.md
└── accomplish/         SKILL.md + script.py (3 subcommands)
```

## Requirements

- [Claude Code](https://claude.ai/code) CLI
- Python 3.8+

## License

MIT — see [LICENSE](LICENSE)

---

Built by [Atlas AI](https://atlas-ai.au)
