# Common Agent Contract

## Overview

Every agent in this framework must be designed against a common contract. This contract defines the minimum required elements of any agent's specification. It ensures agents are governable, explainable, and consistently designed.

The contract is not a prompt template — it is a **design specification**. The prompt is one output of completing the contract.

---

## The Agent Contract

### 1. Identity

| Field | Description |
|-------|-------------|
| **Agent Name** | A clear, descriptive name (e.g., `Project Status Summarizer`) |
| **Identifier** | A stable, unique slug (e.g., `agent-project-status-summary`) |
| **Version** | Semantic version of the agent design (e.g., `1.0`) |
| **Owner** | Name and role of the human responsible for this agent |

### 2. Purpose

- **Primary purpose:** One sentence describing what this agent does and for whom
- **Problem it solves:** What human task or gap does this agent address?
- **Success definition:** How will we know the agent is performing well?

### 3. Scope

**In scope** (explicit list of what the agent does):

- ...
- ...

**Out of scope** (explicit list of what the agent does NOT do):

- ...
- ...

### 4. Knowledge Sources

List the specific knowledge sources this agent is designed to consult:

| Source | Type | Owner | Update Frequency |
|--------|------|-------|-----------------|
| [Source name] | Document / Policy / Data | [Owner name] | [Weekly / Monthly / On change] |

### 5. Inputs

What does the agent receive as input?

- Trigger type: (manual prompt / scheduled / event-driven)
- Input format: (free text / structured data / system event)
- Required context: (what must be present for the agent to operate)

### 6. Outputs

What does the agent produce?

- Output format: (prose / structured markdown / JSON / action)
- Output destination: (human review / connected system / email / file)
- Quality standard: (how will outputs be evaluated?)

### 7. Escalation Rules

Under what conditions must the agent escalate to a human?

- [ ] Ambiguity in the knowledge base
- [ ] Request outside defined scope
- [ ] Confidence below threshold
- [ ] High-stakes or irreversible action
- [ ] Novel situation not covered by existing rules
- Other: ___

### 8. Constraints

What must the agent never do?

- ...
- ...

### 9. Governance

| Field | Value |
|-------|-------|
| **Authorization date** | |
| **Review schedule** | |
| **Audit log required?** | Yes / No |
| **Human override mechanism** | |
| **Suspension procedure** | |

### 10. Prompt Summary

A brief summary of the core instructions given to the agent (not the full prompt — see implementation files for that):

> _[2–4 sentence description of what the agent is instructed to do and how]_

---

## Notes

- This contract must be completed before an agent is deployed
- Changes to scope, knowledge sources, or constraints require a contract revision
- The contract is owned by the agent owner and reviewed on the governance schedule
