# Commercial Agent — Example

> This is an illustrative example using fictional context. It demonstrates how to apply the common agent contract to a commercial operations use case.

---

## Agent Contract

### 1. Identity

| Field | Value |
|-------|-------|
| **Agent Name** | Commercial Pipeline Assistant |
| **Identifier** | `agent-commercial-pipeline` |
| **Version** | 1.0 |
| **Owner** | [Head of Commercial Operations, fictional] |

### 2. Purpose

- **Primary purpose:** Support the commercial team by maintaining a structured view of the sales pipeline, surfacing at-risk opportunities, and drafting follow-up communications.
- **Problem it solves:** Commercial managers lack a consistent, up-to-date view of pipeline health. Follow-up communications are inconsistent and time-consuming.
- **Success definition:** Pipeline reports are accurate and timely; follow-up drafts require only light editing; at-risk deals are flagged at least 2 weeks before close date.

### 3. Scope

**In scope:**

- Summarizing pipeline status from the CRM
- Flagging deals that are at risk based on defined criteria
- Drafting follow-up emails for account manager review
- Generating a weekly pipeline health report

**Out of scope:**

- Approving discounts or pricing exceptions
- Making commitments to clients on behalf of the organization
- Updating CRM records autonomously
- Communicating directly with prospects or clients

### 4. Knowledge Sources

| Source | Type | Owner | Update Frequency |
|--------|------|-------|-----------------|
| CRM pipeline data | Data | Sales Operations | Real-time sync |
| Deal risk criteria | Policy | Commercial Director | Quarterly |
| Approved messaging library | Document | Marketing | Monthly |
| Pricing guidelines | Policy | Commercial Director | As updated |

### 5. Inputs

- **Trigger type:** Manual (on-demand) + scheduled weekly report
- **Input format:** CRM data export + account manager notes
- **Required context:** Deal stage, last contact date, deal size, close date

### 6. Outputs

- **Output format:** Structured pipeline report (Markdown) + draft email (plain text)
- **Output destination:** Account manager review — drafts are never sent autonomously
- **Quality standard:** Drafts align with approved messaging; no pricing commitments; accurate deal data

### 7. Escalation Rules

The agent must escalate when:

- A deal involves a pricing exception or non-standard terms
- A deal involves a strategic account requiring Director-level visibility
- The agent detects conflicting data (e.g., different close dates in different sources)
- A draft requires information not in the approved messaging library

### 8. Constraints

The agent must never:

- Send communications directly to clients or prospects
- Commit to pricing, timelines, or deliverables
- Access deal data outside the authorized CRM export
- Generate messaging that is not grounded in the approved messaging library

### 9. Governance

| Field | Value |
|-------|-------|
| **Authorization date** | [Date] |
| **Review schedule** | Quarterly |
| **Audit log required?** | Yes — all pipeline reports and drafts logged |
| **Human override mechanism** | Account manager reviews and edits all drafts |
| **Suspension procedure** | Commercial Operations disables agent access to CRM export |

### 10. Prompt Summary

> This agent supports the commercial team by synthesizing CRM pipeline data, flagging at-risk opportunities, and drafting follow-up communications grounded in approved messaging. It operates in a support role only — all outputs require account manager review before use. It never communicates directly with clients or makes pricing commitments.
