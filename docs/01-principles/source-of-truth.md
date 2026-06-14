# Source of Truth

## Principle

> Agents must ground their behavior in a maintained, authoritative source of organizational knowledge — not in model memory, internet retrieval, or ad-hoc context.

## The Problem This Solves

Language models are trained on general knowledge. They do not inherently know:

- Your organization's policies
- Your products and pricing
- Your decision-making criteria
- Your current priorities and constraints
- Your team structure and accountability

Without a structured knowledge layer, agents will hallucinate, generalize, or apply incorrect context. The result is outputs that are fluent but wrong for your specific situation.

## What "Source of Truth" Means Here

A source of truth in this framework is:

1. **Explicit** — Written down, structured, and available to the agent
2. **Maintained** — Updated when reality changes
3. **Authoritative** — Designated by the organization as the reliable version
4. **Bounded** — Scoped to what the agent actually needs

This is not a database. It is a **knowledge architecture** — a deliberate set of documents, policies, and facts that agents are designed to consult before acting.

## Layers of Knowledge

| Type | Examples | Owner |
|------|----------|-------|
| Organizational principles | Mission, values, operating model | Leadership |
| Business rules | Approval thresholds, escalation criteria | Operations / Compliance |
| Process documentation | Step-by-step workflows | Process owners |
| Domain knowledge | Product specs, client profiles, market data | Subject matter experts |
| Agent-specific context | Role definition, constraints, instructions | Agent owners |

## Why This Cannot Be Skipped

Agents without a source of truth are uncontrollable. Their behavior varies based on prompt phrasing, model version changes, and contextual noise. Organizations that skip this layer often discover inconsistency at scale — when many agents or many users interact with the system.

## Related Principles

- [`human-first-purpose.md`](human-first-purpose.md) — Humans define and maintain the source of truth
- [`governance-and-evolution.md`](governance-and-evolution.md) — Governance includes managing the knowledge lifecycle
