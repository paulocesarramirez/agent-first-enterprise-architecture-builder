# Public Agent Template

## Purpose

This document provides a **public-safe template** for designing an agent under the
**Agent-First Enterprise Architecture Builder** framework.

This is a reference pattern only.

It is not a production export.
It is not a confidential internal prompt.
It is not a direct copy of the private EmprendHEC operational implementation.

Its purpose is to show how an agent should be described when the architecture comes first and governance is explicit.

---

## 1. Agent identity

### Agent name
`[Agent Name]`

### Agent type
Examples:
- declarative agent
- retrieval-oriented agent
- orchestration agent
- structured workflow agent
- assistant role agent

### Status
Examples:
- example
- placeholder
- reference design
- planned
- active (public-safe description only)

---

## 2. Agent purpose

### Core purpose
State the single most important purpose of the agent.

The purpose should be narrow and clear.

Good pattern:
> This agent exists to support one clearly defined responsibility within the architecture.

Avoid:
- vague multi-purpose descriptions
- agent-as-everything narratives
- hidden responsibilities not justified by architecture

---

## 3. Human value

### Why this agent exists
Describe how this agent reduces friction while preserving or strengthening human capability.

Examples:
- helps humans structure work faster
- monitors change and produces input for human review
- drafts material for human approval
- standardizes repetitive preparation for strategic work

Always make the human role explicit.

---

## 4. Source of truth

### Governing documents
List the categories of documents or architectural sources the agent depends on.

Examples:
- architecture principles
- operating guides
- business rules
- naming conventions
- approved templates
- public knowledge structures

Rule:
the agent must not rely on undocumented parallel knowledge.

---

## 5. Responsibility model

### Single responsibility
Describe the single responsibility principle for the agent.

Template:
> The agent is responsible for `[single responsibility]`.
> The agent is not responsible for `[excluded responsibilities]`.

Examples of excluded responsibilities:
- final approval
- autonomous policy modification
- legal sign-off
- confidential data handling without explicit authorization
- changing system architecture

---

## 6. Inputs

### Typical inputs
Describe the kinds of inputs the agent receives.

Examples:
- structured briefs
- approved templates
- public-safe rules
- task requests
- architecture references
- process checkpoints

Do not include private production inputs in this public template.

---

## 7. Outputs

### Typical outputs
Describe what the agent is expected to produce.

Examples:
- draft recommendations
- structured summaries
- proposed actions
- public-safe reports
- formatted content
- classified observations

The output should always be explainable and auditable.

---

## 8. Boundaries and prohibitions

### Hard boundaries
State what the agent must never do.

Recommended categories:
- must not modify source-of-truth documents without human approval
- must not operate outside its declared role
- must not invent undocumented policy
- must not handle confidential information in public-safe reference environments
- must not present recommendations as final decisions
- must not bypass governance

This section should be explicit, not implied.

---

## 9. Human oversight

### Human-in-the-loop expectations
Describe where human judgment is required.

Template:
- human reviews strategic decisions
- human approves structural changes
- human validates sensitive outputs
- human determines final execution where risk is non-trivial

Principle:
> AI proposes. Humans decide.

---

## 10. Auditability

### Explainability requirement
Describe how the agent should justify its outputs.

Template:
> Every important recommendation should be traceable to an explicit guide, rule, principle, or approved reference.

The goal is:
- transparency
- trust
- traceability
- disciplined operation

---

## 11. Evolution model

### How this agent changes over time
Describe how the agent can evolve.

Recommended rule:
- changes require explicit review
- modifications should be documented
- architecture updates precede behavior changes
- the agent should evolve through governance, not hidden drift

---

## 12. Example skeleton

## Agent Name
`Example Agent`

### Role
Structured support agent for a clearly defined domain.

### Core Purpose
Help users perform one bounded operational or advisory task with consistency and traceability.

### Human Value
Reduce repetitive cognitive friction while preserving human control over strategic outcomes.

### Reads From
- architecture principles
- approved operating guides
- designated templates
- documented rules

### Produces
- structured drafts
- summaries
- recommendations
- standardized outputs

### Must Never
- modify governing documents directly
- invent policy
- bypass human approval
- operate outside defined scope

### Human Oversight
A human must review all strategic, structural, or sensitive outputs.

### Auditability
All significant outputs should reference an explicit source-of-truth element.

---

## 13. Recommended use in this repository

Use this template to create:

- `pm-assistant-example.md`
- `m365-watcher-example.md`
- `commercial-agent-example.md`
- `editorial-agent-example.md`
- `accountant-agent-placeholder.md`
- `legal-agent-placeholder.md`

Each should remain:
- public-safe
- architecture-aligned
- clearly non-confidential
- abstracted when necessary
