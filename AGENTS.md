# Agent Instructions

## Repository Identity

[1-2 sentences: What is this project and what does it do?]

## Context Loading

Agents working on this repository should load context in this order:

1. This file (`AGENTS.md`), which covers repository identity, constraints, and conventions
2. `README.md` for project overview and current state
3. `docs/documentation-standards/` for templates and standards to follow
4. Any domain-specific docs referenced below

## Architectural Constraints

[List non-negotiable constraints that agents must not violate. Examples:]

- [Constraint 1, e.g., "All infrastructure changes require human approval"]
- [Constraint 2, e.g., "No persistent daemon agents except the orchestrator"]
- [Constraint 3]

## Documentation Conventions

- All Markdown files require YAML frontmatter (see `docs/documentation-standards/tagging-strategy.md`)
- New directories require an interior README (see `docs/documentation-standards/interior-readme-template.md`)
- Script files require language-appropriate headers (see `docs/documentation-standards/script-header-*.md`)
- Follow dual-audience commenting (see `docs/documentation-standards/code-commenting-dual-audience.md`)
- Follow writing style conventions (see `docs/documentation-standards/writing-style-guide.md`)

## Commit Messages

- Present tense, imperative mood
- 72-character first line limit
- Reference issues after first line

## Session Pattern

1. Load context (this file + README)
2. Work within defined scope
3. Document changes appropriately
4. Update work-logs if significant work completed
