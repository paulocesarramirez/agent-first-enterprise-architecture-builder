# Agent Design Template

## Purpose

This document provides a **public-safe elemental template** for writing an agent design document
(**Diseño de Agente**) under the
**Agent-First Enterprise Architecture Builder** framework.

It is intentionally generic.

It is designed to allow GitHub Copilot to scaffold new agent design documents while keeping confidential implementation details outside the public repo.

---

## Naming pattern

Recommended filename pattern:

`Design-[Agent-Name].md`

Examples:
- `Design-PM-Assistant.md`
- `Design-M365-Watcher.md`
- `Design-Commercial-Agent.md`
- `Design-Editorial-Assistant.md`
- `Design-Accountant-Agent.md`
- `Design-Legal-Agent.md`

---

## Standard structure

# `[Agent Name]`

## 1. Purpose of this Agent
State:
- why the agent exists
- what problem it solves
- what role it plays inside the architecture

### Template prompt
> This agent exists to support `[single responsibility]` inside the enterprise architecture.

---

## 2. Single Responsibility
Declare the single responsibility principle explicitly.

### Template prompt
> The agent is responsible for `[single responsibility]`.
> The agent is not responsible for `[excluded responsibilities]`.

This section is mandatory.

---

## 3. Human Value
Explain how the agent reduces friction while preserving human agency.

Examples:
- frees time for strategic work
- structures repeated preparation
- creates drafts for human review
- improves consistency without replacing judgment

---

## 4. Position in the Architecture
Describe where the agent sits relative to:
- the source of truth
- the guides
- other agents
- users
- workflows

This section should explain the role, not the internal private implementation.

---

## 5. Governing Sources
List what governs the agent.

Examples:
- architecture principles
- operating guides
- conventions
- approved templates
- knowledge structures

Rule:
the agent must not operate from undocumented parallel knowledge.

---

## 6. Inputs
Describe the kinds of inputs the agent receives.

Examples:
- structured briefs
- forms
- approved content
- architecture references
- process signals
- user requests

Use public-safe examples only.

---

## 7. Outputs
Describe expected outputs.

Examples:
- structured drafts
- summaries
- recommendations
- checklists
- public-safe reports
- formatted deliverables

Outputs should be explainable and reviewable.

---

## 8. Boundaries
State what the agent must never do.

Examples:
- must not modify governing documents without human approval
- must not invent policy
- must not operate outside scope
- must not expose confidential data in public-safe contexts
- must not present drafts as final executive decisions

---

## 9. Autonomy Level
Describe the level of autonomy in qualitative terms.

Examples:
- low
- low-medium
- medium

Support the label with explanation.

### Template prompt
> The agent may `[allowed autonomous behaviors]`, but may not `[disallowed behaviors]` without explicit human authorization.

---

## 10. Human Oversight
State where human review is required.

Examples:
- strategic decisions
- structured changes
- publication
- final approval
- high-risk outputs

Principle:
> AI proposes. Humans decide.

---

## 11. Auditability
Explain how outputs should be justified.

### Template prompt
> All significant outputs should be traceable to a declared source, principle, rule, or approved reference.

---

## 12. Interaction with Other Agents
If relevant, describe high-level interaction boundaries.

Examples:
- hands off work to another agent
- receives structured input from another agent
- does not directly override another agent’s role
- follows a declared contract of interaction

Keep this architectural, not confidential.

---

## 13. Evolution Rule
Document how this agent evolves.

Recommended pattern:
- changes are deliberate
- source-of-truth changes precede behavior changes
- prompt/knowledge changes require review
- no hidden drift

---

## 14. Public-safe note
This public template should never expose:
- real internal prompts
- confidential business logic
- client data
- credentials
- private operational knowledge
- hidden production configuration

If needed, publish placeholders instead.

---

## Minimal example skeleton

# Example Agent

## 1. Purpose
This agent exists to support `[single responsibility]`.

## 2. Single Responsibility
Responsible for `[responsibility]`.
Not responsible for `[exclusions]`.

## 3. Human Value
Describe the benefit to human work.

## 4. Position in the Architecture
Describe the architectural role.

## 5. Governing Sources
- source 1
- source 2

## 6. Inputs
- input 1
- input 2

## 7. Outputs
- output 1
- output 2

## 8. Boundaries
- boundary 1
- boundary 2

## 9. Autonomy Level
Describe the autonomy level.

## 10. Human Oversight
Describe review requirements.

## 11. Auditability
Describe justification requirements.

## 12. Interaction with Other Agents
Describe interaction constraints.

## 13. Evolution Rule
Describe controlled evolution.
