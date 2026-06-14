# Common Agent Contract

## Purpose

This document defines the common contract that every agent designed under the
**Agent-First Enterprise Architecture Builder** framework should follow.

This is a public-safe reference contract.

It is intended to help architects, contributors, and GitHub Copilot maintain coherence across all public-safe agent design examples in this repository.

---

## Why a common contract exists

An agent ecosystem should not grow through improvisation.

Without a common contract, organizations tend to accumulate:
- overlapping responsibilities
- hidden assumptions
- duplicated logic
- unclear authority boundaries
- weak governance

A common contract ensures that agents remain:
- coherent
- legible
- auditable
- scalable
- aligned with architecture

---

## Contract Principle 1 — Architecture First

Every agent must be designed as a consumer of the architecture.

Agents do not define truth.
Agents read and apply truth.

That means:
- the architecture precedes the agent
- the architecture constrains the agent
- the architecture explains the agent

---

## Contract Principle 2 — Single Responsibility

Every agent must have one clearly declared responsibility.

The responsibility must be:
- narrow enough to be understood
- important enough to justify the role
- explicit enough to prevent overlap

Good pattern:
> one role, one responsibility, clear exclusions

Bad pattern:
> a vague assistant expected to do everything

---

## Contract Principle 3 — Human Judgment Remains Central

Agents may:
- structure
- accelerate
- classify
- summarize
- propose

Agents may not replace human judgment in strategic or sensitive decisions.

Each agent design must explicitly state:
- where human approval is required
- which outputs are only drafts or recommendations
- which actions are out of scope without human review

---

## Contract Principle 4 — Source of Truth Only

Agents must only operate from declared sources of truth.

They must not rely on:
- undocumented tribal knowledge
- hidden memory not approved by architecture
- parallel knowledge stores outside governance
- improvised rules not documented in the system

Every agent design should state what governs it.

---

## Contract Principle 5 — Transparency and Auditability

Agent behavior must be explainable.

Each important output should be traceable to:
- a guide
- a principle
- a rule
- a template
- an approved reference

If an agent cannot justify an output from a declared source, the output should be treated as ungrounded.

---

## Contract Principle 6 — Bounded Autonomy

Agents may be autonomous inside declared boundaries.

Those boundaries must be explicit.

Each agent should define:
- what it can do
- what it can recommend
- what it must not do
- when it must defer
- what requires escalation or approval

Bounded autonomy is strength.
Unbounded autonomy is risk.

---

## Contract Principle 7 — Controlled Evolution

Agents should not evolve silently.

Changes to agent design should be:
- deliberate
- documented
- reviewed
- aligned with architecture updates

If architecture changes, agent behavior may change.
If architecture does not change, agent drift should be treated as a governance problem.

---

## Contract Principle 8 — Reduction of Friction with Purpose

Agents exist to reduce friction in meaningful work.

They should:
- save time
- improve consistency
- support clarity
- free humans for higher-value thinking

They should not:
- create noise
- create dependency without value
- overcomplicate interaction
- obscure responsibility

---

## Minimum contract fields for every public-safe agent design

Every public-safe agent design in this repository should declare:

1. **Agent Name**
2. **Purpose**
3. **Human Value**
4. **Single Responsibility**
5. **Source of Truth**
6. **Inputs**
7. **Outputs**
8. **Hard Boundaries**
9. **Human Oversight**
10. **Auditability Rule**
11. **Evolution Rule**

---

## Example statement

A public-safe example agent contract should resemble this pattern:

- This agent exists for one clearly bounded responsibility.
- This agent reads only approved architecture and declared guides.
- This agent produces explainable outputs.
- This agent does not bypass human judgment.
- This agent remains inside explicit governance boundaries.

---

## Relationship to examples

This contract should govern all public-safe example agents in this repository, including:

- PM Assistant example
- M365 Watcher example
- Commercial Agent example
- Editorial Assistant example
- Accountant Agent placeholder
- Legal Agent placeholder

These are examples and placeholders only.
They are not direct exports of the private implementation.

---

## Final principle

A strong agent ecosystem is not built by adding more agents.

It is built by ensuring that every agent is:
- grounded
- governed
- explainable
- bounded
- human-aligned
