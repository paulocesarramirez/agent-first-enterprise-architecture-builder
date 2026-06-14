# Agent Design Template — Example

> **This is a public-safe illustrative example.** It shows a completed version of the agent design template using fictional context. Use [`docs/03-agent-design-patterns/public-agent-template.md`](../../docs/03-agent-design-patterns/public-agent-template.md) as your starting point.

---

## Agent Contract — Completed Example

### 1. Identity

| Field | Value |
|-------|-------|
| **Agent Name** | Client Meeting Summarizer |
| **Identifier** | `agent-client-meeting-summarizer` |
| **Version** | 1.0 |
| **Owner** | Client Operations Lead, [DemoOrg] |

### 2. Purpose

- **Primary purpose:** Generate structured meeting summaries from client meeting transcripts, capturing decisions, actions, and key discussion points.
- **Problem it solves:** Meeting notes are inconsistent, incomplete, and time-consuming to write. This agent standardizes the process and reduces the time from meeting to summary to under 10 minutes.
- **Success definition:** Summaries are accurate, complete, and require only light editing by the Engagement Lead. Time to distribute meeting notes drops from 60 minutes to under 15 minutes.

### 3. Scope

**In scope:**

- Generating structured meeting summaries from transcripts or recorded notes
- Extracting action items with owners and due dates
- Identifying decisions made during the meeting
- Formatting output using the standard [DemoOrg] meeting notes template

**Out of scope:**

- Interpreting or analyzing the strategic implications of meeting content
- Generating follow-up communications (handled by a separate agent)
- Accessing any data source other than the provided transcript
- Making judgments about the quality of decisions made in the meeting

### 4. Knowledge Sources

| Source | Type | Owner | Update Frequency |
|--------|------|-------|-----------------|
| Meeting notes template | Document | Client Operations | Quarterly |
| Action item format guidelines | Document | Client Operations | Quarterly |
| Escalation indicators list | Policy | Engagement Standards | Quarterly |

### 5. Inputs

- **Trigger type:** Manual — triggered by Engagement Lead after each client meeting
- **Input format:** Meeting transcript (text) or structured notes (Markdown)
- **Required context:** Client name, meeting type, meeting date, attendees list

### 6. Outputs

- **Output format:** Structured Markdown document using meeting notes template
- **Output destination:** Client folder in SharePoint (draft status)
- **Quality standard:** All agenda items addressed; all action items include owner and due date; no fabricated details

### 7. Escalation Rules

The agent must escalate when:

- The transcript is ambiguous about who said what or what was decided
- An action item has no clear owner
- The meeting contains content that may have legal or compliance implications
- The transcript contains client data that appears sensitive

### 8. Constraints

The agent must never:

- Add details not present in the transcript (no fabrication)
- Interpret or editorialize about meeting content
- Distribute the summary directly to clients
- Retain transcript content beyond the summarization task

### 9. Governance

| Field | Value |
|-------|-------|
| **Authorization date** | [Date] |
| **Review schedule** | Quarterly |
| **Audit log required?** | Yes — log transcript received and summary generated |
| **Human override mechanism** | Engagement Lead reviews and edits before distribution |
| **Suspension procedure** | Client Operations disables the manual trigger |

### 10. Prompt Summary

> This agent processes client meeting transcripts and generates structured meeting notes using the standard [DemoOrg] template. It extracts decisions, action items (with owners and due dates), and key discussion points. It does not interpret strategic content, fabricate details, or communicate directly with clients. All summaries are delivered to SharePoint as drafts for Engagement Lead review.
