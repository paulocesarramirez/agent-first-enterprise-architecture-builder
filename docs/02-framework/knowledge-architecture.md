# Knowledge Architecture

## What Is Knowledge Architecture?

Knowledge architecture is the deliberate design of how an organization's knowledge is **structured, stored, maintained, and made accessible** — specifically with the goal of making it machine-actionable by AI agents.

This is distinct from knowledge management, which focuses on human access and sharing. Knowledge architecture optimizes for **agent reliability**.

## Why This Matters

An agent's quality ceiling is determined by the quality of the knowledge it has access to. No prompt engineering, fine-tuning, or model upgrade can compensate for absent, outdated, or unstructured organizational knowledge.

## Knowledge Domains

A complete knowledge architecture covers the following domains:

### 1. Foundational Knowledge
- Organizational mission and values
- Operating principles
- Strategic priorities

### 2. Operational Knowledge
- Business processes and workflows
- Decision rules and approval thresholds
- Roles and responsibilities

### 3. Domain Knowledge
- Products and services
- Client and market information
- Regulatory and compliance requirements

### 4. Contextual Knowledge
- Current projects and initiatives
- Constraints and resource availability
- Recent decisions and rationale

### 5. Agent-Specific Knowledge
- Agent role definition and purpose
- Behavioral constraints
- Output expectations and standards

## Structural Requirements

For knowledge to be reliably used by agents, it must be:

| Requirement | Description |
|-------------|-------------|
| **Written** | Not in people's heads — documented explicitly |
| **Structured** | Organized in a consistent, parseable format |
| **Authoritative** | Designated as the correct version |
| **Current** | Updated when underlying reality changes |
| **Scoped** | Each agent gets the knowledge it needs, not everything |
| **Versioned** | Changes are tracked and reversible |

## Knowledge Maintenance Model

Knowledge is not static. The architecture must account for:

- **Scheduled reviews** — Regular audits of each knowledge domain
- **Event-triggered updates** — Policy changes, product launches, reorgs
- **Agent feedback** — Flagging knowledge gaps or conflicts discovered during operation
- **Ownership** — Every knowledge domain has a named human owner

## Anti-Patterns to Avoid

| Anti-Pattern | Problem |
|--------------|---------|
| Using chat history as knowledge | Volatile, unstructured, not authoritative |
| Storing knowledge only in human memory | Not accessible to agents |
| One monolithic knowledge document | Hard to maintain, scope creep |
| No ownership assigned | Knowledge becomes stale with no accountability |

## Related Documents

- [`architecture-layers.md`](architecture-layers.md) — Knowledge is Layer 1
- [`docs/01-principles/source-of-truth.md`](../01-principles/source-of-truth.md) — The principle behind this design
- [`examples/public-safe-architecture-example/`](../../examples/public-safe-architecture-example/) — A worked example
