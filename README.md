# Programming with AI Workshop

Welcome to the **Programming with AI Workshop** for the Applied Research team.

## Overview

This hands-on workshop teaches you how to effectively use AI assistants (like GitHub Copilot) in your development workflow while maintaining code quality through automated enforcement.

## Workshop Phases

| Phase | Duration | Focus |
|-------|----------|-------|
| 1. The AI Workflow | 15 min | Core loop: Plan, Build, Review; agents vs autocomplete |
| 2. Zero-Hallucination Setup | 25 min | Environment setup, dependency management, baseline rules |
| 3. The Hard Enforcement | 20 min | Linting configuration, pre-commit hooks, repository lockdown |
| 4. Feature Development | 50 min | Plan, build overly complex code, watch it get blocked, refactor |

## Resources

- **Workshop Materials**: [GitHub Pages](./pages/)
- **Sample Data**: `data/online_retail.xlsx`
- **Source Code**: `src/`
- **Reports**: `reports/`

## Quick Start

```bash
# Create virtual environment
python -m venv .venv

# Activate (Windows)
.venv\Scripts\activate

# Activate (macOS/Linux)
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Set up pre-commit hooks
pre-commit install
```

## Directory Structure

```
├── .github/
│   └── copilot-instructions.md  # AI assistant rules
├── scripts/                     # Utility scripts
├── data/                        # Datasets
├── pages/                       # GitHub Pages content
├── src/                         # Source code
├── reports/                     # Analysis reports
├── pyproject.toml               # Project configuration
├── .pre-commit-config.yaml      # Pre-commit hooks
└── requirements.txt             # Dependencies
```
