# GitHub Copilot Instructions for this Repository

## Repository Purpose & Positioning
This repository is the public architecture, framework, and reference patterns for:
**Agent-First Enterprise Architecture Builder** — a reference framework for designing, governing, and evolving enterprise systems that place AI agents at the center of business operations. Its thesis: **agents are first-class citizens** of the enterprise, not add-ons.

Always preserve this category definition:
- This project is an **architecture**, a **framework**, and a **mindset**.
- It is NOT the private production implementation of EmprendHEC's operational agentic system.
- The live demo is **one private implementation example**; this repo shares only the **reusable, public-safe layer**.

## Human-Centered Rule
All generated content must reflect **Agent-First Infrastructure, Human-First Purpose**:
- AI/agents amplify human capability; human judgment remains central.
- Governance, auditability, and transparency are required.
- Documentation should reduce friction without reducing human strategic involvement.

## Architecture Thinking
When assisting with design or documentation:
- Always consider the **full stack**: knowledge layer → governance layer → generation layer → execution layer.
- Ask "what is the agent's purpose?" before proposing any design.
- Reference existing framework files in `docs/02-framework/` when applicable.

## Guided Implementation ("implement this for my company")
When a user asks to implement, adopt, or reproduce this framework for their own organization (e.g., "I want this implemented for my company"):
1. **Run the diagnostic first** — follow `docs/05-copilot-implementation/implementation-diagnostic.md` to determine the user's Microsoft stack and preferred build style, producing a recommended path (No-Code = Declarative agents, Low-Code = Copilot Studio, Pro-Code = Azure AI Foundry + Microsoft Agent Framework, or Hybrid).
2. **Then follow the playbook** — use `docs/05-copilot-implementation/implementation-playbook.md` to guide the build step by step, using this repo as the source of truth.
3. Keep the diagnostic simple and conversational; never block on perfect answers; infer safe defaults and note assumptions.
4. Keep everything public-safe: never collect or echo secrets, tenant IDs, or confidential business detail.

## Public-Safe Content Rule
This is the governing constraint for everything generated — files, docs, code scaffolding, examples, diagrams, and templates.

**Always:**
- Use only public-safe, generic, non-confidential information.
- Keep agent examples abstracted, genericized, and clearly labeled as examples or placeholders.
- Maintain explicit boundaries between public examples and private implementation.

**Never:**
- Invent or expose internal operational details of EmprendHEC, including private prompts, confidential workflows, live decision rules, or proprietary data structures (unless explicitly approved for public release).
- Include secrets, credentials, endpoints, customer/client data, PII, or internal business logic.
- Export the private working system directly, or imply illustrative examples are production-ready.

**If an artifact would require confidential information:**
- Do not fabricate or infer it.
- Generate a public-safe placeholder and explicitly label the missing content as private implementation detail.

## Allowed Artifacts
Copilot may generate:
- markdown documentation, diagrams, and example templates
- placeholder config files and public-safe code scaffolds
- generic agent design patterns and file/folder structures

Do **not** generate executable code for production deployment.

## Documentation & Writing Style
Prioritize (in order): **clarity → explicit structure → modularity → governance → public-safe examples**.

- Use precise, architectural language with a professional documentation tone.
- Use strong structural headings, Markdown bullet points, and tables.
- Favor **concrete examples** over abstract theory.
- Keep files **focused** — one concept per document.

## File & Naming Conventions
- Follow `docs/05-copilot-implementation/naming-conventions.md`.
- Prefer descriptive, architecture-oriented prefixes: `architecture-*`, `framework-*`, `public-safe-*`, `example-*`, `placeholder-*`, `governance-*`.
- Use placeholder names like `[YourOrg]`, `[YourSystem]`, `[YourProcess]` when in doubt.
- New docs go in the appropriate `docs/0X-` folder.
- New examples go in `examples/` and must end in `.example.md`.
- Diagrams go in `examples/diagrams/` and use `.mmd` (Mermaid) format.
- Do not create files outside the defined folder structure without discussion.
- Do not modify `docs/01-principles/` without explicit instruction — these are foundational.

## Key Files to Reference
- `docs/00-overview/architecture-overview.md` — Start here for context
- `docs/02-framework/architecture-layers.md` — The core layered model
- `docs/03-agent-design-patterns/common-agent-contract.md` — Standard agent structure
- `docs/05-copilot-implementation/repo-implementation-guidelines.md` — Entry point for implementing the framework for an organization
- `docs/05-copilot-implementation/implementation-diagnostic.md` — Stack & build-style diagnostic (run first)
- `docs/05-copilot-implementation/implementation-playbook.md` — Step-by-step build per path
- `docs/05-copilot-implementation/safe-scaffolding-instructions.md` — How to add new content safely
- `docs/05-copilot-implementation/naming-conventions.md` — File and folder naming rules
