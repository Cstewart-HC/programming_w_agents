# Programming with AI Workshop

Welcome to the **Programming with AI Workshop** for the Applied Research team.

**Workshop Materials**: [GitHub Pages](https://cstewart-hc.github.io/programming_w_agents/)

## Overview

This hands-on workshop teaches you how to effectively use AI assistants (like GitHub Copilot) in your development workflow while maintaining code quality through automated enforcement.

## Workshop Phases

| Phase | Duration | Focus |
|-------|----------|-------|
| 0. Preflight Check | 5 min | Verify environment (VS Code, Copilot, Python, Git) |
| 1. The AI Workflow | 10 min | Core loop: Plan, Build, Review; agents vs autocomplete |
| 2. Deterministic Setup | 20 min | Environment setup, dependency management, baseline rules |
| 3. Reviewing Enforcement | 10 min | Inspect linting configuration and pre-commit hooks |
| 4. Feature Development | 45 min | Plan, build overly complex code, watch it get blocked, refactor |

## Resources

- **Workshop Materials**: [GitHub Pages](https://cstewart-hc.github.io/programming_w_agents/)
- **Full Workshop Guide**: [docs/workshop.html](docs/workshop.html)
- **Handouts**:
  - [Handout 1: Applied Analytics Engineering Principles](docs/handouts/principles.html)
  - [Handout 2: Copilot UI & Cheat Sheet](docs/handouts/copilot-cheatsheet.html)
  - [Handout 3: Fallback Configurations](docs/handouts/fallback-configs.html)
- **Sample Data**: `data/retail_sample.csv` (December 2010 transactions)
- **Full Dataset**: `data/online_retail.xlsx`
- **Source Code**: `src/`
- **Notebooks**: `notebooks/`

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
├── data/
│   ├── retail_sample.csv        # Workshop sample (Dec 2010)
│   └── online_retail.xlsx       # Full UCI dataset
├── notebooks/                   # Jupyter notebooks
├── docs/                        # GitHub Pages content
│   ├── index.html
│   ├── workshop.html
│   └── handouts/
├── scripts/                     # Utility scripts
├── src/                         # Source code
├── reports/                     # Analysis reports
├── pyproject.toml               # Project configuration
├── .pre-commit-config.yaml      # Pre-commit hooks
└── requirements.txt             # Dependencies
```
