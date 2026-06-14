# GitHub Copilot Instructions

## Project Context

This repository is the **Agent-First Enterprise Architecture Builder** — a public reference framework for designing, governing, and evolving enterprise systems that place AI agents at the center of business operations.

The architecture is built on the principle that **agents are first-class citizens** of the enterprise, not add-ons. Everything in this repo supports that thesis.

## How to Help in This Repo

When assisting with this repository, Copilot should:

### Tone and Style
- Write in a **clear, structured, professional tone**
- Favor **concrete examples** over abstract theory
- Use **Markdown headers, bullet points, and tables** for all documentation
- Keep files **focused** — one concept per document

### Architecture Thinking
- Always consider the **full stack**: knowledge layer → governance layer → generation layer → execution layer
- Ask "what is the agent's purpose?" before proposing any design
- Reference existing framework files in `docs/02-framework/` when applicable

### Content Safety
- **Never include** proprietary system names, credentials, or internal process details
- Examples must be **illustrative and generic** — suitable for public viewing
- When in doubt, use placeholder names like `[YourOrg]`, `[YourSystem]`, `[YourProcess]`

### File Conventions
- Follow naming conventions in `docs/05-copilot-implementation/naming-conventions.md`
- New docs go in the appropriate `docs/0X-` folder
- New examples go in `examples/` and must end in `.example.md`
- Diagrams go in `examples/diagrams/` and use `.mmd` (Mermaid) format

### What NOT to Do
- Do not generate executable code for production deployment
- Do not create files outside the defined folder structure without discussion
- Do not add agent prompts that reference private internal systems
- Do not modify `docs/01-principles/` without explicit instruction — these are foundational

## Key Files to Reference

- `docs/00-overview/architecture-overview.md` — Start here for context
- `docs/02-framework/architecture-layers.md` — The core layered model
- `docs/03-agent-design-patterns/common-agent-contract.md` — Standard agent structure
- `docs/05-copilot-implementation/safe-scaffolding-instructions.md` — How to add new content safely
