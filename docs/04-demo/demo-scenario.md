# Demo Scenario

## Scenario: Weekly Operations Rhythm

This scenario illustrates how multiple agents work together within the agent-first architecture to support a routine operational workflow.

> **Note:** All organization names, people, and data are fictional. This is an illustrative scenario only.

---

## Context

[DemoOrg] runs a weekly operations review every Monday. Historically, preparing for this meeting required:

- 2 hours of project status gathering by the PMO
- 1 hour of content review by the editorial team
- 30 minutes of pipeline update by commercial ops
- A manual compilation of all inputs into a single briefing document

Total: ~3.5 hours of preparation work each week.

---

## How the Agent-First Architecture Changes This

### Friday (automated)

**M365 Watcher Agent** runs its weekly digest:
- Generates aggregate M365 activity summary
- Flags any anomalies in usage patterns
- Posts digest to IT Operations channel in Teams

### Monday 08:00 (scheduled)

**PM Assistant Agent** runs:
- Reads project tracking data from Planner
- Cross-references against active project list and health criteria in SharePoint
- Generates structured status report
- Posts to PMO shared document for review

**Commercial Pipeline Agent** runs:
- Reads CRM export
- Flags at-risk deals based on defined criteria
- Drafts pipeline health summary
- Posts to Commercial Ops review queue

### Monday 09:00 (manual trigger)

**Editorial Review Agent** is triggered for any content submitted for the week's review:
- Reviews drafts against style guide and brand voice
- Returns annotated feedback to authors
- Flags any items requiring compliance review

### Monday 10:00

PMO Lead reviews and approves PM status report (15 min vs. 2 hours previously).
Commercial Ops reviews pipeline summary (10 min vs. 30 min previously).
Operations briefing is compiled with reviewed agent outputs (20 min vs. 90 min previously).

---

## What Made This Work

1. **Knowledge was structured** — Agents had authoritative, current sources to consult
2. **Scope was defined** — Each agent did its specific job without overstepping
3. **Humans reviewed** — No agent output was used without human approval
4. **Escalation worked** — Two items were flagged and escalated; both were resolved before the briefing

## Key Metrics (Illustrative)

| Task | Before | After | Reduction |
|------|--------|-------|-----------|
| PMO status prep | 2h | 15min | ~88% |
| Pipeline summary | 30min | 10min | ~67% |
| Briefing compilation | 90min | 20min | ~78% |
| Total | 3.5h | 45min | ~79% |

---

## What This Scenario Does NOT Illustrate

- The specific knowledge content used by any agent
- The actual prompts powering each agent
- Real integrations or API configurations
- Any specific organization's data or processes
