# Architecture Overview

## What Is This?

The **Agent-First Enterprise Architecture Builder** is a public reference framework for designing enterprise systems where AI agents are first-class participants — not afterthoughts or bolt-ons.

This is not a product. It is an **architectural stance** backed by a structured framework.

## The Core Thesis

> In an agent-first enterprise, the question is not "where do we add AI?" — it is "how do we design the entire system so agents can reliably act on behalf of the organization?"

This requires rethinking how knowledge is structured, how decisions are governed, how outputs are generated, and how execution is orchestrated.

## The Four Layers

The architecture is organized into four interdependent layers:

| Layer | Name | Purpose |
|-------|------|---------|
| 1 | **Knowledge Layer** | Structured, authoritative organizational knowledge |
| 2 | **Agent Governance Layer** | Rules, boundaries, and oversight for agent behavior |
| 3 | **Generation Layer** | AI-assisted content, reasoning, and decision support |
| 4 | **Execution Layer** | Actions taken in connected enterprise systems |

Each layer builds on the one below it. Agents cannot execute well without governance. Governance cannot function without knowledge. See [`docs/02-framework/architecture-layers.md`](../02-framework/architecture-layers.md) for the detailed breakdown.

## What This Repo Contains

- **Principles** (`docs/01-principles/`) — The non-negotiable foundations
- **Framework** (`docs/02-framework/`) — The four-layer architectural model
- **Agent Design Patterns** (`docs/03-agent-design-patterns/`) — Reusable agent structures
- **Demo Content** (`docs/04-demo/`) — Illustrative scenarios
- **Implementation Guidance** (`docs/05-copilot-implementation/`) — How this repo itself is built and maintained
- **FAQ** (`docs/06-faq/`) — Common questions answered

## What This Repo Does NOT Contain

This is a public-safe view of the framework. Private agent configurations, internal business rules, and proprietary system integrations are intentionally excluded. See [`docs/04-demo/what-is-public-vs-private.md`](../04-demo/what-is-public-vs-private.md) for details.

## Where to Start

1. Read this document
2. Review the [core principles](../01-principles/human-first-purpose.md)
3. Study the [architecture layers](../02-framework/architecture-layers.md)
4. Explore the [agent design patterns](../03-agent-design-patterns/README.md)
