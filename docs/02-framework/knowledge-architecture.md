# Knowledge Architecture Layer

## Purpose

This document expands **Layer 1** of the
**Agent-First Enterprise Architecture Builder** framework: the **Knowledge Architecture Layer**.

This is the **source of truth** — the foundation every other layer consumes. Before any agent is governed, any capability is generated, or any tool is configured, the organization defines *how it thinks, works, decides, and evolves* as structured knowledge.

This document is public-safe and intended for learning, adaptation, and implementation guidance.

---

## Why this layer comes first

The framework deliberately starts here, not with tools. An organization that defines its knowledge first can generate coherent capability from it. An organization that starts with tools tends to produce:

- fragmented logic
- duplicated decisions
- contradictions between teams and systems
- weak governance and poor adaptability

> The system should adapt to the organization — not the other way around.

The Knowledge Architecture Layer is what makes capability *generated from architecture* possible.

---

## What this layer defines

The Knowledge Architecture Layer documents the organization's operating logic as explicit, structured knowledge:

### Principles
The foundational beliefs that guide decisions and behavior.

### Processes
How work actually flows — the steps, sequences, and handoffs.

### Rules
The constraints, criteria, and decision logic that govern action.

### Semantics
Shared vocabulary and meaning, so humans and agents interpret terms consistently.

### Decision boundaries
What can be decided automatically, what requires human judgment, and where the line sits.

### Intended agent behavior
The expectations any agent must honor when it consumes this knowledge.

---

## Characteristics of good knowledge architecture

This layer should be:

- **Explicit** — written down, not implicit or tribal
- **Structured** — organized so humans and AI can navigate it
- **Reusable** — usable across many agents and use cases
- **Transversal** — shared, not siloed per team
- **Human-curated** — maintained and approved by people
- **Authoritative** — when an agent disagrees with it, the knowledge wins

---

## Typical outputs

Examples of what this layer produces:

- operating guides
- architecture documents
- agent principles and conventions
- approved templates
- semantic glossaries
- governance rules and decision criteria

---

## Grounding the knowledge — the "IQ" layers

In a Microsoft environment, this curated knowledge is made operational by grounding agents in defined knowledge sources, which Microsoft exposes as composable "IQ" grounding layers. An organization selects what matches its needs.

| Grounding layer | Grounds agents in | Typical use |
|-----------------|-------------------|-------------|
| **Work IQ** | Microsoft 365 work content and signals | Day-to-day work grounded in the organization's own content |
| **Web IQ** | Public web knowledge | Up-to-date external information |
| **Foundry IQ** | Knowledge curated via Azure AI Foundry | Pro-code, governed custom knowledge |
| **Fabric IQ** | Enterprise data modeled in Microsoft Fabric | Analytics- and data-grounded reasoning |

> The reference implementation at EmprendHEC grounds primarily in **Work IQ** and **Web IQ** today. The framework extends to **Foundry IQ** and **Fabric IQ** as well, because the right combination depends on each organization.

The principle holds across every layer: **agents reason from curated knowledge, and humans govern what that knowledge contains.**

---

## Relationship to the other layers

**Knowledge Architecture** (defines truth) ← *this layer*
→ **Agent Governance** (protects coherence)
→ **Capability Generation** (enables operational design)
→ **Execution** (runs the system in practice)

Everything downstream depends on this layer. If the knowledge changes, governed capability can evolve with it — see [`../01-principles/governance-and-evolution.md`](../01-principles/governance-and-evolution.md).

---

## Human-centered interpretation

This layer keeps **purpose above tooling**. By documenting how the organization thinks before choosing how it executes, it preserves human strategic involvement and prevents tools from silently dictating how the organization works.

This is the foundation of **Agent-First Infrastructure, Human-First Purpose.**

---

## Public vs private application

This repository shares the public **structure** of the knowledge layer.

A private implementation may include:

- real business rules and decision criteria
- actual processes with internal names and steps
- live knowledge-base content
- confidential organizational logic

Those private details must not appear in the public repo. The public repo shares the **knowledge architecture pattern**, not the operational knowledge itself.

See [`../01-principles/public-repo-boundary.md`](../01-principles/public-repo-boundary.md).

---

## Final summary

The Knowledge Architecture Layer:

1. Defines the organization's operating logic as **explicit, structured knowledge**
2. Serves as the **single source of truth** for every other layer
3. Stays **human-curated, authoritative, and reusable**
4. Is grounded operationally through chosen **IQ** layers

Architecture comes first. This layer is where it begins.

---

## Related documents

- [`architecture-layers.md`](architecture-layers.md) — The full four-layer model
- [`agent-governance-layer.md`](agent-governance-layer.md) — How agents are governed when consuming this knowledge
- [`../01-principles/source-of-truth.md`](../01-principles/source-of-truth.md) — The principle behind this layer
