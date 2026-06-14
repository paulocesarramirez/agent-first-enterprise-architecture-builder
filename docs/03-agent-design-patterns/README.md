# Agent Design Patterns

This folder contains the standard structures and illustrative examples for designing agents within the Agent-First Enterprise Architecture framework.

## Contents

### Foundation

| File | Description |
|------|-------------|
| [`common-agent-contract.md`](common-agent-contract.md) | The standard structure every agent must follow |
| [`public-agent-template.md`](public-agent-template.md) | A blank template for designing new agents |

### Illustrated Examples

| File | Agent Type | Status |
|------|------------|--------|
| [`pm-assistant-example.md`](pm-assistant-example.md) | Project management assistant | Example |
| [`m365-watcher-example.md`](m365-watcher-example.md) | Microsoft 365 activity monitor | Example |
| [`commercial-agent-example.md`](commercial-agent-example.md) | Commercial operations support | Example |
| [`editorial-agent-example.md`](editorial-agent-example.md) | Editorial content production | Example |

### Placeholders (Coming Soon)

| File | Agent Type |
|------|------------|
| [`accountant-agent-placeholder.md`](accountant-agent-placeholder.md) | Financial operations support |
| [`legal-agent-placeholder.md`](legal-agent-placeholder.md) | Legal review and compliance |

## How to Use These Patterns

1. Start with the [`common-agent-contract.md`](common-agent-contract.md) to understand the required structure
2. Use the [`public-agent-template.md`](public-agent-template.md) when designing a new agent
3. Review the examples for your closest analogous use case
4. Apply the framework to your specific context — adapting scope, knowledge sources, and constraints

## Design Principles for Agents

Every agent in this framework must be:

- **Grounded** — it operates only from a declared **source of truth**
- **Single-purpose** — it has one clearly bounded responsibility
- **Human-aligned** — human judgment stays central; the agent proposes, humans decide
- **Bounded** — it has explicit **hard boundaries** and **escalation rules**
- **Explainable** — every important output is **auditable** back to a declared source
- **Governed in its evolution** — it changes only through deliberate, approved updates

These map directly to the eleven minimum contract fields in
[`common-agent-contract.md`](common-agent-contract.md):
Agent Name, Purpose, Human Value, Single Responsibility, Source of Truth, Inputs,
Outputs, Hard Boundaries, Human Oversight, Auditability Rule, and Evolution Rule.

See [`docs/02-framework/agent-governance-layer.md`](../02-framework/agent-governance-layer.md) for the governance requirements that apply to all agents.
