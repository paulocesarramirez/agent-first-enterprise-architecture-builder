# Naming Conventions

## Purpose

This document defines the **file and folder naming rules** for this repository. Consistent naming keeps the framework navigable, makes Copilot-generated content predictable, and reinforces the public-safe boundary.

It is referenced by [`.github/copilot-instructions.md`](../../.github/copilot-instructions.md) and applies to every new artifact.

---

## General rules

- Use **kebab-case** for files and folders: `lowercase-words-with-hyphens`.
- Use **descriptive, architecture-oriented** names; avoid vague names like `final`, `v1-final`, `new`, `temp`.
- One concept per file; keep documents focused.
- Use `/` for paths; never include drive letters or external folders in references.
- Avoid confidential or project-specific titles in public files.

---

## Folder structure

New content goes in the appropriate existing folder:

| Folder | Contains |
|--------|----------|
| `docs/00-overview/` | orientation, category definition, demo scope |
| `docs/01-principles/` | foundational principles — **do not modify without explicit instruction** |
| `docs/02-framework/` | the four-layer framework |
| `docs/03-agent-design-patterns/` | agent contract, templates, and examples |
| `docs/04-demo/` | the EmprendHEC demo, screenshots, public/private boundary |
| `docs/05-copilot-implementation/` | templates, diagnostic, playbook, scaffolding rules |
| `docs/06-faq/` | frequently asked questions |
| `examples/` | public-safe examples (see suffix rule) |
| `examples/diagrams/` | Mermaid diagrams |
| `assets/` | logos, visuals, diagrams |

Do not create files outside this structure without discussion.

---

## File type conventions

| Type | Pattern | Example |
|------|---------|---------|
| Documentation | `kebab-case-name.md` | `architecture-overview.md` |
| Example | `kebab-case-name.example.md` | `business-rules.example.md` |
| Diagram | `kebab-case-name.mmd` (Mermaid) | `architecture-layers.mmd` |
| Numbered guide | `NN-Guide-Type-Topic.md` | `01-Operating-Principles.md` |
| Agent design doc | `Design-Agent-Name.md` | `Design-Commercial-Agent.md` |

> Examples **must** end in `.example.md`. Diagrams **must** use `.mmd`.

---

## Descriptive prefixes

When a prefix clarifies intent, prefer these:

- `architecture-*` — architectural structure or models
- `framework-*` — framework definitions
- `governance-*` — governance and control
- `public-safe-*` — explicitly public-safe artifacts
- `example-*` — illustrative examples
- `placeholder-*` — content awaiting a real (private) implementation

---

## Placeholder names

When real values would be confidential, use clearly-labeled placeholders so any reader can substitute their own:

| Placeholder | Use for |
|-------------|---------|
| `[YourOrg]` | the adopting organization |
| `[YourSystem]` | a system or platform |
| `[YourProcess]` | a process or workflow |
| `[single responsibility]` | an agent's one job |
| `[exclusions]` | what an agent does not do |

Use placeholders whenever in doubt rather than inventing specifics.

---

## When implementing in your own tenant

The same spirit applies to artifacts you create in **your** environment (SharePoint guides, agent design docs):

- Keep names descriptive and consistent (e.g., `Guia-Operativa-[Area].docx`, `Design-[Agent-Name].md`).
- Avoid `final`/`v1-final`; let versioning and governance track changes.
- Mirror the public structure (Guides, Agents, Reports) so the source of truth stays navigable.

---

## Related documents

- [safe-scaffolding-instructions.md](safe-scaffolding-instructions.md) — how to add content safely
- [repo-implementation-guidelines.md](repo-implementation-guidelines.md) — implementing the framework
- [guide-template.md](guide-template.md) — guide naming and structure
- [agent-design-template.md](agent-design-template.md) — agent design naming and structure
