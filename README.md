<!--
---
title: "Project Template Repository"
description: "Standardized scaffolding for AI-native, RAG-optimized project repositories"
author: "VintageDon (https://github.com/vintagedon/)"
date: "2026-03-28"
version: "2.0"
status: "Active"
tags:
  - type: project-root
  - domain: [templates, documentation]
  - tech: [markdown, yaml, python, powershell]
related_documents:
  - "[RadioAstronomy.io Organization](https://github.com/radioastronomyio)"
  - "[Proxmox Astronomy Lab](https://github.com/vintagedon/proxmox-astronomy-lab)"
---
-->

# Project Template Repository

[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

> Standardized scaffolding for AI-native, RAG-optimized project repositories with documentation templates, agent instructions, and development workflow structure.

This repository provides the foundational structure for new projects within [RadioAstronomy.io](https://github.com/radioastronomyio). It establishes consistent patterns for documentation, AI agent collaboration, and development workflow — designed to be forked or used as a GitHub template when starting new work.

---

## Overview

Modern development increasingly involves AI agents as collaborators — code assistants, documentation generators, and autonomous workers. Traditional project scaffolding doesn't account for this reality. Files are organized for humans, context is implicit, and agents must rediscover project state every session.

This template addresses that gap through **RAG-optimized documentation** (YAML frontmatter, semantic structure, controlled vocabulary), **AGENTS.md** (persistent context that agents load at session start), and **work logs** (development history that agents can reference).

---

## Architecture

The template provides three layers: documentation infrastructure, agent scaffolding, and project structure.

### Documentation Infrastructure

| Component | Purpose |
|-----------|---------|
| `docs/documentation-standards/` | Template library (READMEs, KB articles, script headers) |
| YAML frontmatter | Enables RAG retrieval and filtering |
| Interior README pattern | Self-documenting directories with navigation links |
| Tagging strategy | Controlled vocabulary for metadata |

### Agent Scaffolding

| Component | Purpose |
|-----------|---------|
| `AGENTS.md` | Repository identity, constraints, context loading order, session pattern |

### Project Structure

| Component | Purpose |
|-----------|---------|
| `work-logs/` | Development history (date-based entries, gathered into milestones as patterns emerge) |
| `spec/` | Specifications and deployment definitions |
| `internal-files/` | Reference docs, GDRs, review materials (gitignored in public repos) |
| `shared/` | Cross-project utilities |
| `staging/` | Pre-commit staging area |

---

## Project Status

| Area | Status | Description |
|------|--------|-------------|
| Documentation Templates | ✅ Complete | Primary, interior, KB, worklog templates |
| Script Headers | ✅ Complete | Python, Shell, PowerShell |
| Tagging Strategy | ✅ Complete | Controlled vocabulary guide |
| Code Commenting Guide | ✅ Complete | Dual-audience (human + AI) methodology |
| Editor Config | ✅ Complete | VSCode, markdownlint, cspell |
| Shared Utilities | 🔄 Growing | Tree generator |

---

## Repository Structure

```markdown
project-template-repository/
├── docs/                     # Documentation
│   └── documentation-standards/  # Template library
├── internal-files/           # Reference docs (gitignored in public repos)
├── shared/                   # Cross-project utilities
├── spec/                     # Specifications, deployment definitions
├── staging/                  # Pre-commit staging area
├── work-logs/                # Development history
├── AGENTS.md                 # Agent context loading instructions
├── CODE_OF_CONDUCT.md        # Community standards
├── CONTRIBUTING.md           # Contribution guidelines
├── LICENSE                   # MIT License (code)
├── LICENSE-DATA              # CC-BY-4.0 (data/content)
├── SECURITY.md               # Security policy
├── cspell.json               # Spell checker config
└── .markdownlint.json        # Markdown linter config
```

---

## Documentation Templates

The template library in `docs/documentation-standards/` provides consistent formatting.

### Document Templates

| Template | Use For |
|----------|---------|
| [primary-readme-template.md](docs/documentation-standards/primary-readme-template.md) | Repository root README |
| [interior-readme-template.md](docs/documentation-standards/interior-readme-template.md) | Directory READMEs |
| [general-kb-template.md](docs/documentation-standards/general-kb-template.md) | Standalone documents (guides, specs, reports, runbooks) |
| [worklog-readme-template.md](docs/documentation-standards/worklog-readme-template.md) | Work log entries |

### Script Headers

| Template | Use For |
|----------|---------|
| [script-header-python.md](docs/documentation-standards/script-header-python.md) | All `.py` files |
| [script-header-shell.md](docs/documentation-standards/script-header-shell.md) | All `.sh` files |
| [script-header-powershell.md](docs/documentation-standards/script-header-powershell.md) | All `.ps1` files |

### Guidelines

| Document | Use For |
|----------|---------|
| [tagging-strategy.md](docs/documentation-standards/tagging-strategy.md) | Building YAML frontmatter vocabulary |
| [code-commenting-dual-audience.md](docs/documentation-standards/code-commenting-dual-audience.md) | Writing comments for humans and AI |

---

## Quick Start

### Using as GitHub Template

1. Click "Use this template" on GitHub
2. Name your new repository
3. Clone locally
4. Customize:
   - Edit `AGENTS.md` with your project's identity and constraints
   - Edit `README.md` with your project's overview
   - Build your domain vocabulary in `docs/documentation-standards/tagging-strategy.md`
   - Copy `.gitignore.example` to `.gitignore` and adjust for public/private

### Template Selection

```
Is it the repository root README?
├─ Yes → primary-readme-template.md
└─ No: Is it a directory README?
        ├─ Yes → interior-readme-template.md
        └─ No: Is it a standalone document?
                └─ Yes → general-kb-template.md
```

---

## License

- **Code**: [MIT License](LICENSE)
- **Data/Content**: [CC-BY-4.0](LICENSE-DATA)

---

Last Updated: March 28, 2026 | Status: Active
