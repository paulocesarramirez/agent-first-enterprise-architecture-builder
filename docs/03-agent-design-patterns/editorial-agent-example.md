# Editorial Agent — Example

> This is an illustrative example using fictional context. It demonstrates how to apply the common agent contract to a content review and editorial use case.

---

## Agent Contract

### 1. Identity

| Field | Value |
|-------|-------|
| **Agent Name** | Editorial Review Assistant |
| **Identifier** | `agent-editorial-review` |
| **Version** | 1.0 |
| **Owner** | [Head of Content, fictional] |

### 2. Purpose

- **Primary purpose:** Review draft content for alignment with editorial standards, brand voice, and factual consistency before human editorial review.
- **Problem it solves:** Editorial teams spend significant time on first-pass reviews of drafts that don't yet meet baseline standards. This agent handles the first-pass triage.
- **Success definition:** Drafts flagged by the agent have measurably more issues than those approved; editor time on first-pass review is reduced by >40%.

### 3. Scope

**In scope:**

- Checking drafts against the editorial style guide
- Flagging inconsistencies with the approved brand voice guidelines
- Identifying factual claims that require verification
- Checking for structural and formatting compliance
- Producing an annotated review with specific, actionable feedback

**Out of scope:**

- Making final editorial decisions
- Publishing or distributing content
- Rewriting content without explicit instruction
- Assessing strategic or business value of content

### 4. Knowledge Sources

| Source | Type | Owner | Update Frequency |
|--------|------|-------|-----------------|
| Editorial style guide | Document | Head of Content | Quarterly |
| Brand voice guidelines | Document | Brand Team | As updated |
| Approved terminology list | Document | Content + Legal | Monthly |
| Content type templates | Document | Content Team | Quarterly |

### 5. Inputs

- **Trigger type:** Manual — triggered when a draft is submitted for review
- **Input format:** Draft document (Markdown or Word)
- **Required context:** Content type, target audience, publication channel

### 6. Outputs

- **Output format:** Annotated review document with flagged issues and suggested improvements
- **Output destination:** Author and editor review queue
- **Quality standard:** All style guide violations flagged; no false positives > 10%; feedback is specific and actionable

### 7. Escalation Rules

The agent must escalate when:

- A draft contains claims that may have legal or compliance implications
- The draft references topics outside the agent's knowledge base (e.g., new products not yet documented)
- The draft is flagged for content policy concerns
- The volume of issues exceeds a threshold suggesting the draft needs significant rework before review

### 8. Constraints

The agent must never:

- Approve content for publication
- Rewrite substantial portions of a draft without being explicitly asked
- Share drafts or reviews outside the designated review system
- Apply editorial standards from a different content type than the one specified

### 9. Governance

| Field | Value |
|-------|-------|
| **Authorization date** | [Date] |
| **Review schedule** | Quarterly — including style guide alignment check |
| **Audit log required?** | Yes — all reviews logged with version of style guide used |
| **Human override mechanism** | Editor can accept or reject any agent flag |
| **Suspension procedure** | Head of Content disables submission trigger |

### 10. Prompt Summary

> This agent performs a first-pass editorial review of submitted draft content. It checks alignment with the style guide, brand voice, and approved terminology. It produces an annotated review with specific feedback for the author and editor. It does not make final decisions, rewrite content, or approve publication. It escalates when content raises legal, compliance, or policy concerns.
