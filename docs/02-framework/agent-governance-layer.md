# Agent Governance Layer

## Purpose

This document expands **Layer 2** of the
**Agent-First Enterprise Architecture Builder** framework: the **Agent Governance Layer**.

Where the [Knowledge Architecture Layer](architecture-layers.md) defines *what is true*, the Agent Governance Layer defines *how agents are allowed to act on that truth*.

This document is public-safe and intended for learning, adaptation, and implementation guidance.

---

## Why this layer exists

Agents are not the architecture. They are **governed components** that consume the source of truth and act within explicit limits.

Without a governance layer, agentic systems tend to:

- drift beyond their intended scope
- contradict each other across teams and tasks
- act on knowledge they were never meant to touch
- become impossible to audit, explain, or correct

This layer protects the organization from uncontrolled or incoherent agent behavior.

### Core rule

> AI accelerates, structures, and proposes.
> **Humans decide.**

---

## What this layer governs

### 1. Grounding
Every agent reads from the **source of truth**. Agents do not improvise rules or silently rewrite the knowledge they depend on.

### 2. Scope and boundaries
Each agent has a **defined purpose** and explicit limits. It does only what its declared responsibility allows, and escalates anything beyond it.

### 3. Human oversight
Agents must keep humans in the critical path for consequential decisions. Humans can always override, suspend, or redirect an agent.

### 4. Auditability
Agent actions and outputs must be **traceable** — what was produced, from what knowledge, and on whose approval.

### 5. Controlled evolution
Agent behavior, prompts, and core guides change only through **human-approved**, deliberate change — never through hidden drift.

---

## The Common Agent Contract

In this framework, every agent is defined by a shared, explicit contract before it is built. This is the practical instrument of governance.

A governed agent declares:

- **Purpose** — the human goal it serves
- **Scope** — what it is allowed to do
- **Boundaries** — what it must never do, and when it must escalate
- **Knowledge sources** — the curated grounding it reads from
- **Human checkpoints** — where human approval is required
- **Auditability** — how its actions can be reviewed

> See the [common agent contract](../03-agent-design-patterns/common-agent-contract.md) for the standard structure, and the [public agent template](../03-agent-design-patterns/public-agent-template.md) for a reusable starting point.

---

## Governance across build approaches

The same governance principles apply regardless of how an agent is built. The governance layer is the constant; the build technology is the variable.

| Build approach | Platform | Governance still requires |
|----------------|----------|---------------------------|
| **Declarative agents** | Microsoft 365 Copilot | Defined scope, curated grounding, human oversight |
| **Low-code agents** | Copilot Studio | Bounded orchestration, traceable actions, approved knowledge |
| **Pro-code agents** | Azure AI Foundry + Microsoft Agent Framework | Explicit boundaries, auditability, controlled change |

A more sophisticated build approach never means weaker governance. Every agent, at every level, stays grounded, bounded, auditable, and human-governed.

---

## What this layer does *not* do

- It does not define the organization's knowledge — that is the [Knowledge Architecture Layer](architecture-layers.md).
- It does not generate workflows or operating patterns — that is the Capability Generation Layer.
- It does not run the agents in production tools — that is the [Execution Layer](microsoft-execution-layer.md).

This layer sets the **rules of conduct** that every other layer must respect.

---

## Relationship to the other layers

**Knowledge Architecture** (defines truth)
→ **Agent Governance** (protects coherence) ← *this layer*
→ **Capability Generation** (enables operational design)
→ **Execution** (runs the system in practice)

Governance sits deliberately between knowledge and capability: nothing becomes operational until it is governed.

---

## Human-centered interpretation

This layer is where **Agent-First Infrastructure, Human-First Purpose** is enforced in practice.

It keeps:

- purpose above capability
- principles above convenience
- human judgment above uncontrolled automation
- transparency above opaque behavior

Infrastructure can be highly agentic; **meaning, purpose, and direction remain human.**

---

## Public vs private application

This repository shares the public version of the governance layer.

A private implementation may include:

- confidential agent prompts and instructions
- real knowledge-source references
- internal approval and escalation rules
- production integration and access configuration

Those private details must not appear in the public repo. The public repo shares the **governance pattern**, not the operational implementation.

See [`../01-principles/public-repo-boundary.md`](../01-principles/public-repo-boundary.md).

---

## Final summary

The Agent Governance Layer ensures that every agent is:

1. **Grounded** in the source of truth
2. **Bounded** by a defined purpose and explicit limits
3. **Overseen** by humans on consequential decisions
4. **Auditable** in its actions and outputs
5. **Governed** through deliberate, human-approved change

Agents are powerful — but in this framework, they are always **governed components**, never ungoverned actors.

---

## Related documents

- [`architecture-layers.md`](architecture-layers.md) — The full four-layer model
- [`microsoft-execution-layer.md`](microsoft-execution-layer.md) — Where governed agents run
- [`../01-principles/governance-and-evolution.md`](../01-principles/governance-and-evolution.md) — The principle behind controlled evolution
- [`../03-agent-design-patterns/common-agent-contract.md`](../03-agent-design-patterns/common-agent-contract.md) — The standard agent structure
