# Public Agent Template

> Copy this template to design a new agent. Replace all `[placeholder]` values with your specific details. Delete this instruction block before finalizing.

---

## Agent Contract

### 1. Identity

| Field | Value |
|-------|-------|
| **Agent Name** | [Descriptive name] |
| **Identifier** | `agent-[short-slug]` |
| **Version** | 1.0 |
| **Owner** | [Name, Role] |

### 2. Purpose

- **Primary purpose:** [One sentence]
- **Problem it solves:** [What human task does this replace or augment?]
- **Success definition:** [How will performance be measured?]

### 3. Scope

**In scope:**

- [Specific task 1]
- [Specific task 2]
- [Specific task 3]

**Out of scope:**

- [Excluded task 1]
- [Excluded task 2]

### 4. Knowledge Sources

| Source | Type | Owner | Update Frequency |
|--------|------|-------|-----------------|
| [Source 1] | [Document/Policy/Data] | [Owner] | [Frequency] |
| [Source 2] | [Document/Policy/Data] | [Owner] | [Frequency] |

### 5. Inputs

- **Trigger type:** [Manual / Scheduled / Event-driven]
- **Input format:** [Free text / Structured / System event]
- **Required context:** [What must be provided?]

### 6. Outputs

- **Output format:** [Prose / Markdown / JSON / Action]
- **Output destination:** [Human review / System / Email / File]
- **Quality standard:** [How will output quality be assessed?]

### 7. Escalation Rules

The agent must escalate to a human when:

- [ ] Knowledge base is ambiguous or missing
- [ ] Request is outside defined scope
- [ ] High-stakes or irreversible action is required
- [ ] [Add domain-specific rule]

### 8. Constraints

The agent must never:

- [Constraint 1]
- [Constraint 2]

### 9. Governance

| Field | Value |
|-------|-------|
| **Authorization date** | [Date] |
| **Review schedule** | [Quarterly / Annual / On trigger] |
| **Audit log required?** | [Yes / No] |
| **Human override mechanism** | [Describe] |
| **Suspension procedure** | [Describe] |

### 10. Prompt Summary

> [2–4 sentences describing the core instructions for this agent]

---

## Checklist Before Deployment

- [ ] All fields in the contract are completed
- [ ] Knowledge sources are confirmed as current and accessible
- [ ] Escalation rules have been tested
- [ ] Owner has reviewed and approved
- [ ] Governance review is scheduled
