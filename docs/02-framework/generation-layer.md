# Capability Generation Layer

## Purpose

This document expands **Layer 3** of the
**Agent-First Enterprise Architecture Builder** framework: the **Capability Generation Layer**.

This is the **bridge from architecture to operational form**. It is where governed knowledge becomes usable capability — workflows, agent responsibilities, collaboration structures, and implementation blueprints — without losing coherence with the source of truth.

This document is public-safe and intended for learning, adaptation, and implementation guidance.

---

## Why this layer exists

A defined knowledge architecture and a clear governance model are necessary but not yet operational. Something has to translate them into concrete, usable capability.

This layer does exactly that. It allows the organization to move from **abstract architecture** to **working capability** in a controlled, repeatable way.

### Important distinction

> This layer does not replace architecture. It **depends on** architecture.

Capability is generated *from* the knowledge and governance layers. If the architecture changes, generated capability can evolve in a governed way — never the reverse.

---

## What this layer generates

From the governed source of truth, this layer produces:

### Workflows
Concrete sequences of work, derived from documented processes.

### Agent responsibilities
The specific purpose and scope each agent will hold, expressed as a contract.

### Role patterns
Reusable definitions of how humans and agents collaborate on a task.

### Collaboration structures
How work, people, and agents are organized to operate together.

### Implementation blueprints
The plans that tell the Execution Layer what to build and how.

---

## From architecture to the right agent

This is where **GitHub Copilot** becomes a practical accelerator. With the architecture and source of truth defined, Copilot helps generate *exactly the agents each use case requires* — at the right level of sophistication.

| Build approach | Platform | When to use |
|----------------|----------|-------------|
| **Declarative agents** | Microsoft 365 Copilot | Lightweight agents grounded in M365 content, defined through configuration |
| **Low-code agents** | Copilot Studio | Orchestrated agents that compose multiple IQ grounding layers without heavy code |
| **Pro-code agents** | Azure AI Foundry + Microsoft Agent Framework | Fully custom agents needing advanced control, tools, and governance |

The architecture is the constant; the build approach is the variable. A company picks the level that fits each use case — but every generated agent still reasons from the same governed source of truth and respects the same governance rules.

---

## How generation stays governed

Generated capability is only valuable if it stays coherent. This layer respects the layers above it:

- **Grounded** — every generated agent reads from the source of truth
- **Bounded** — each agent receives a defined purpose and explicit limits (the [common agent contract](../03-agent-design-patterns/common-agent-contract.md))
- **Human-approved** — new capability is reviewed before it becomes operational
- **Traceable** — what was generated, from what knowledge, remains auditable

Generation accelerates the organization; it does not bypass its governance.

---

## What this layer does *not* do

- It does not define the knowledge — that is the [Knowledge Architecture Layer](knowledge-architecture.md).
- It does not set the rules of conduct — that is the [Agent Governance Layer](agent-governance-layer.md).
- It does not run agents in production tools — that is the [Execution Layer](microsoft-execution-layer.md).

This layer **translates** governed architecture into capability ready for execution.

---

## Relationship to the other layers

**Knowledge Architecture** (defines truth)
→ **Agent Governance** (protects coherence)
→ **Capability Generation** (enables operational design) ← *this layer*
→ **Execution** (runs the system in practice)

This layer sits deliberately between governance and execution: nothing is built until it has been generated *from* governed architecture.

---

## Human-centered interpretation

This layer keeps **principles above convenience**. Capability is shaped by the organization's documented logic and human judgment — not by whatever a tool happens to make easy.

By generating capability from architecture, the organization scales without surrendering its strategic intent. This is **Agent-First Infrastructure, Human-First Purpose** in practice.

---

## Public vs private application

This repository shares the public **patterns** for generating capability.

A private implementation may include:

- real workflow definitions tied to live operations
- production agent responsibilities and prompts
- internal collaboration and approval structures
- confidential implementation blueprints

Those private details must not appear in the public repo. The public repo shares the **generation pattern**, not the operational capability itself.

See [`../01-principles/public-repo-boundary.md`](../01-principles/public-repo-boundary.md).

---

## Final summary

The Capability Generation Layer:

1. **Translates** governed architecture into usable capability
2. Produces workflows, agent responsibilities, and implementation blueprints
3. Uses **GitHub Copilot** to generate the right agent for each use case (declarative, low-code, or pro-code)
4. Stays **grounded, bounded, human-approved, and traceable**

It is the bridge: architecture in, operational capability out.

---

## Related documents

- [`architecture-layers.md`](architecture-layers.md) — The full four-layer model
- [`knowledge-architecture.md`](knowledge-architecture.md) — The source of truth this layer consumes
- [`agent-governance-layer.md`](agent-governance-layer.md) — The rules generated capability must respect
- [`microsoft-execution-layer.md`](microsoft-execution-layer.md) — Where generated capability runs
- [`../03-agent-design-patterns/common-agent-contract.md`](../03-agent-design-patterns/common-agent-contract.md) — The standard agent structure
