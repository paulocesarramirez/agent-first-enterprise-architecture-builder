# Repository Implementation Guidelines

## What this document is

This is the **entry point** for anyone who wants to use this repository to implement the
**Agent-First Enterprise Architecture Builder** framework in their own organization.

If you say to Copilot or GitHub Copilot:

> _"I want this implemented for my company, using this repo as the reference,"_

this document explains the journey, and points to the two tools that drive it:

1. **[implementation-diagnostic.md](implementation-diagnostic.md)** — a short diagnostic that determines your path.
2. **[implementation-playbook.md](implementation-playbook.md)** — step-by-step build instructions for that path.

---

## The core idea

This repository is the **public, reusable framework** — the architecture, principles, patterns, and templates. It is **not** a turnkey product and it is **not** the private operational system behind the EmprendHEC demo.

To implement it, you don't copy a system. You **reproduce the four layers** in your own Microsoft environment, using this repo as your **source of truth for the pattern**:

```
Knowledge  →  Governance  →  Capability Generation  →  Execution
```

Your organization supplies its own knowledge, governance decisions, and execution context. Copilot helps you assemble them — adapted to your Microsoft stack and your preferred build style.

---

## The implementation journey

### Step 1 — Run the diagnostic
Open [implementation-diagnostic.md](implementation-diagnostic.md). Copilot asks a few simple questions about your Microsoft 365 plan, Copilot subscriptions, Azure/AI Foundry access, Power Platform/Fabric, preferred build style, and cost posture. It returns a recommended **path**:

| Path | Build surface |
|------|---------------|
| **No-Code** | Declarative agents (Microsoft 365 Copilot agent builder) |
| **Low-Code** | Microsoft Copilot Studio |
| **Pro-Code** | Azure AI Foundry + Microsoft Agent Framework |
| **Hybrid** | A mix, grown over time |

### Step 2 — Follow the playbook
Open [implementation-playbook.md](implementation-playbook.md). It walks you through:
- **Part 1 — Universal foundation** (Knowledge + Governance + first agent design) — same for everyone.
- **Part 2 — Path-specific build** (the Capability Generation layer) — depends on your path.
- **Part 3 — Execution & governance** — putting it to work inside Microsoft 365.

### Step 3 — Stay public-safe
Throughout, follow [safe-scaffolding-instructions.md](safe-scaffolding-instructions.md) and [naming-conventions.md](naming-conventions.md) so anything you publish stays public-safe and consistent.

---

## What you'll use from this repo

| You need… | Use… |
|-----------|------|
| The big picture | [../00-overview/architecture-overview.md](../00-overview/architecture-overview.md) |
| The four-layer model | [../02-framework/architecture-layers.md](../02-framework/architecture-layers.md) |
| The shared agent contract | [../03-agent-design-patterns/common-agent-contract.md](../03-agent-design-patterns/common-agent-contract.md) |
| A guide template | [guide-template.md](guide-template.md) |
| An agent design template | [agent-design-template.md](agent-design-template.md) |
| Worked agent examples | [../03-agent-design-patterns/](../03-agent-design-patterns/) |
| Proof it works | [../04-demo/demo-architecture.md](../04-demo/demo-architecture.md) |

---

## Guardrails for any implementation

These hold no matter which path you choose:

- **Architecture first.** Structure the knowledge and governance before building agents.
- **Single source of truth.** Agents read from your knowledge base, not parallel undocumented knowledge.
- **AI proposes, humans decide.** Keep human approval where it matters.
- **Controlled evolution.** Changes to guides and prompts are reviewed; no hidden drift.
- **Public-safe boundary.** Never publish prompts, keys, tenant detail, client data, or confidential business logic. See [../04-demo/what-is-public-vs-private.md](../04-demo/what-is-public-vs-private.md).

---

## Related documents

- [implementation-diagnostic.md](implementation-diagnostic.md) — start here
- [implementation-playbook.md](implementation-playbook.md) — then here
- [safe-scaffolding-instructions.md](safe-scaffolding-instructions.md) — keep it public-safe
- [naming-conventions.md](naming-conventions.md) — naming rules
- [model-and-build-surface-selection.md](model-and-build-surface-selection.md) — model and role selection
- [../02-framework/responsible-ai-and-governance-hierarchy.md](../02-framework/responsible-ai-and-governance-hierarchy.md) — governance hierarchy
- [../06-faq/can-any-company-use-this.md](../06-faq/can-any-company-use-this.md) — yes, and why
