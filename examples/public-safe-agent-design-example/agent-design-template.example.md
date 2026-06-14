# Agent Design Template — Example

> **This is a public-safe illustrative example.** It shows a completed version of the canonical agent template using fictional context. It follows the same section structure as [`docs/03-agent-design-patterns/public-agent-template.md`](../../docs/03-agent-design-patterns/public-agent-template.md), which you should use as your blank starting point.

---

## Agent Contract — Completed Example

### 1. Agent identity

| Field | Value |
|-------|-------|
| **Agent name** | Client Meeting Summarizer |
| **Identifier** | `agent-client-meeting-summarizer` |
| **Agent type** | Structured workflow agent |
| **Status** | Reference design (public-safe) |
| **Version** | 1.0 |
| **Owner** | Client Operations Lead, [DemoOrg] |

---

### 2. Agent purpose

- **Core purpose:** Generate structured meeting summaries from client meeting transcripts, capturing decisions, actions, and key discussion points.
- **Problem it solves:** Meeting notes are inconsistent, incomplete, and time-consuming to write. This agent standardizes the process and reduces the time from meeting to summary.
- **Success definition:** Summaries are accurate, complete, and require only light editing by the Engagement Lead before distribution.

The purpose is narrow and singular: it summarizes, it does not advise.

---

### 3. Human value

This agent reduces the repetitive cognitive friction of writing meeting notes so that humans can spend their time on judgment, not transcription.

- It drafts; the Engagement Lead approves.
- It standardizes preparation; the human owns the relationship and the decisions.
- It accelerates routine documentation; it never replaces human accountability for client outcomes.

The human role remains explicit at every step: **the agent proposes a draft, a human decides what is distributed.**

---

### 4. Source of truth

| Source | Type | Owner | Update Frequency |
|--------|------|-------|-----------------|
| Meeting notes template | Document | Client Operations | Quarterly |
| Action item format guidelines | Document | Client Operations | Quarterly |
| Escalation indicators list | Policy | Engagement Standards | Quarterly |

Rule: the agent must rely only on these governing documents and the provided transcript. It must not rely on undocumented parallel knowledge.

---

### 5. Responsibility model

> The agent is responsible for **producing a structured draft summary from a single meeting transcript.**
> The agent is **not** responsible for:
>
> - interpreting or analyzing the strategic implications of meeting content
> - generating follow-up communications (handled by a separate agent)
> - accessing any data source other than the provided transcript
> - making judgments about the quality of decisions made in the meeting

---

### 6. Inputs

- **Trigger type:** Manual — triggered by the Engagement Lead after each client meeting.
- **Input format:** Meeting transcript (text) or structured notes (Markdown).
- **Required context:** Client name, meeting type, meeting date, attendees list.

Do not include private production inputs in this public example.

---

### 7. Outputs

- **Output format:** Structured Markdown document using the standard meeting notes template.
- **Output destination:** Client folder in SharePoint (draft status).
- **Quality standard:** All agenda items addressed; all action items include owner and due date; no fabricated details.

Every output is explainable and auditable.

---

### 8. Boundaries and prohibitions

The agent must never:

- add details not present in the transcript (no fabrication)
- interpret or editorialize about meeting content
- distribute the summary directly to clients
- retain transcript content beyond the summarization task
- present its draft as a final, approved record

These boundaries are explicit, not implied.

---

### 9. Human oversight

Human judgment is required where risk is non-trivial. The agent must escalate to a human when:

- the transcript is ambiguous about who said what or what was decided
- an action item has no clear owner
- the meeting contains content that may have legal or compliance implications
- the transcript contains client data that appears sensitive

In all cases, the Engagement Lead reviews and edits the draft before distribution.

> AI proposes. Humans decide.

---

### 10. Auditability

| Field | Value |
|-------|-------|
| **Authorization date** | [Date] |
| **Review schedule** | Quarterly |
| **Audit log required?** | Yes — log transcript received and summary generated |
| **Human override mechanism** | Engagement Lead reviews and edits before distribution |
| **Suspension procedure** | Client Operations disables the manual trigger |

Every significant output is traceable to the meeting notes template and the provided transcript.

---

### 11. Evolution model

- Changes to scope, sources, or boundaries require explicit review by Client Operations.
- Modifications are documented before behavior changes.
- Architecture and template updates precede any change to agent behavior — the agent evolves through governance, not hidden drift.

---

### Prompt summary

> This agent processes client meeting transcripts and generates structured meeting notes using the standard [DemoOrg] template. It extracts decisions, action items (with owners and due dates), and key discussion points. It does not interpret strategic content, fabricate details, or communicate directly with clients. All summaries are delivered to SharePoint as drafts for Engagement Lead review.
