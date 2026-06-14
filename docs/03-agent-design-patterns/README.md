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
| [`editorial-agent-example.md`](editorial-agent-example.md) | Content review and editorial | Example |

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

- Every agent has a **single primary purpose**
- Every agent has a **named owner**
- Every agent has explicit **escalation rules**
- Every agent operates from a **defined knowledge base**
- Every agent has clear **output standards**

See [`docs/02-framework/agent-governance-layer.md`](../02-framework/agent-governance-layer.md) for the governance requirements that apply to all agents.
