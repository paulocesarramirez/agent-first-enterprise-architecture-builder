# Demo Scenario

## Scenario: Weekly Operations Rhythm

This scenario illustrates how the EmprendHEC agents work together within the agent-first architecture to support a routine operational workflow.

> **Note:** Timings, data, and individual steps below are **illustrative and public-safe**. They show the *pattern* of collaboration, not EmprendHEC's confidential operational detail.

---

## Context

A mission-driven organization like EmprendHEC runs a recurring operations review. Historically, preparing for it required:

- Project and information status gathering by whoever leads delivery
- Content review by the editorial function
- Commercial pipeline update by commercial ops
- A manual compilation of all inputs into a single briefing document

Total: several hours of preparation work each cycle.

---

## How the Agent-First Architecture Changes This

### Friday (automated)

**M365 Watcher Agent** runs its weekly digest:
- Generates aggregate M365 activity summary
- Flags any anomalies in usage patterns
- Posts digest to IT Operations channel in Teams

### Monday 08:00 (scheduled)

**PM Assistant** runs:
- Reads project and task data from Planner
- Cross-references against the active project list and health criteria in SharePoint
- Generates a structured status report
- Posts to the shared document for human review

**Commercial Agent** runs:
- Reviews incoming opportunities against the commercial guide's qualification criteria
- Flags prospects that are not yet qualified (missing required inputs)
- Drafts a pipeline health summary using official tariffs and templates
- Posts to the commercial review queue

### Monday 09:00 (manual trigger)

**Editorial Assistant** is triggered for any content submitted for the cycle's review:
- Reviews drafts against the brand guide and editorial voice
- Returns annotated feedback to authors
- Flags any items requiring escalation

### Monday 10:00

The delivery lead reviews and approves the PM status report.
Commercial ops reviews the pipeline summary.
The operations briefing is compiled from reviewed agent outputs — each in a fraction of the time the manual process required.

---

## What Made This Work

1. **Knowledge was structured** — Agents had authoritative, current sources to consult
2. **Scope was defined** — Each agent did its specific job without overstepping
3. **Humans reviewed** — No agent output was used without human approval
4. **Escalation worked** — Two items were flagged and escalated; both were resolved before the briefing

## Key Metrics (Illustrative)

> These figures are illustrative placeholders that show the *shape* of the improvement, not measured EmprendHEC results.

| Task | Before | After | Reduction |
|------|--------|-------|-----------|
| Status prep | 2h | 15min | ~88% |
| Pipeline summary | 30min | 10min | ~67% |
| Briefing compilation | 90min | 20min | ~78% |
| Total | 3.5h | 45min | ~79% |
---

## Watch the Demo

The Agents League Hackathon demo video shows this scenario — and the full framework — operating live inside Microsoft 365:

[![Video Demo - Agent First Enterprise Architecture Builder - Agents League Hackathon](https://img.youtube.com/vi/9_NN3AMkOaw/maxresdefault.jpg)](https://www.youtube.com/watch?v=9_NN3AMkOaw)

▶️ [Watch on YouTube: Agent-First Enterprise Architecture Builder — Agents League Hackathon](https://www.youtube.com/watch?v=9_NN3AMkOaw)
---

## What This Scenario Does NOT Illustrate

- The specific knowledge content used by any agent
- The actual prompts powering each agent
- Real integrations or API configurations
- EmprendHEC's confidential data, pricing, or decision criteria
