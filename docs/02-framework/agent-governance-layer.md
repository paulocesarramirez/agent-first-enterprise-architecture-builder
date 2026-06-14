# Agent Governance Layer

## Purpose

The Agent Governance Layer is the organizational and structural framework that determines **what agents are allowed to do, how they are overseen, and who is accountable** when they act.

This layer sits between the knowledge foundation and the generation/execution capabilities. Without it, capable agents become uncontrollable agents.

## Core Components

### 1. Agent Registry

Every deployed agent must be registered with:

- **Name and identifier** — Unique, descriptive name
- **Purpose statement** — One-sentence description of what the agent does
- **Owner** — Named human responsible for the agent's behavior
- **Scope** — Explicit list of what the agent is and is not permitted to do
- **Deployment date** — When the agent was authorized for use
- **Review schedule** — When the agent will next be evaluated

### 2. Authorization Model

Not every agent should have access to everything. The governance layer defines:

| Access Type | Governed By |
|-------------|-------------|
| Knowledge domains the agent can read | Scope definition |
| Systems the agent can interact with | Integration permissions |
| Actions the agent can take autonomously | Authority boundaries |
| Decisions the agent must escalate | Escalation rules |

### 3. Escalation Framework

Agents must know when to stop and ask. Escalation is triggered by:

- Ambiguity in the knowledge base
- Requests outside the agent's defined scope
- Outputs that exceed a confidence or impact threshold
- Novel situations not covered by existing rules

### 4. Audit and Review

Agent behavior must be reviewable. The governance layer requires:

- Output logging at an appropriate level of detail
- Periodic sampling and human review
- Incident reporting when things go wrong
- Governance reviews on a defined schedule

### 5. Override and Suspension

Humans must always be able to:

- Override a specific agent output
- Redirect an agent to a different approach
- Suspend an agent temporarily
- Retire an agent permanently

These controls are not optional. They are requirements of the human-first principle.

## Governance Tiers

Governance should be proportional to consequence:

| Tier | Agent Type | Governance Level |
|------|------------|-----------------|
| 1 | Drafting and summarization | Light — sample review, owner accountability |
| 2 | Recommendation and analysis | Medium — structured review, documented decisions |
| 3 | Action and execution | Heavy — approval workflows, full audit trail |

## Related Documents

- [`architecture-layers.md`](architecture-layers.md) — Layer 2 context
- [`docs/01-principles/governance-and-evolution.md`](../01-principles/governance-and-evolution.md) — The principle this implements
- [`docs/03-agent-design-patterns/common-agent-contract.md`](../03-agent-design-patterns/common-agent-contract.md) — How governance is expressed per agent
