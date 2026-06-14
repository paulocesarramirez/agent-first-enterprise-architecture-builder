# Agent Boundaries — Example

> **This is a public-safe illustrative example.** All organization names and agent configurations are fictional. This demonstrates how an organization might define the boundaries for agents operating within a specific domain.

---

## [DemoOrg] — Agent Boundary Definitions

*Version 1.0 | Owned by: [IT Operations Lead] | Reviewed: Quarterly*

---

### Purpose

This document defines the boundaries for all agents deployed at [DemoOrg]. Boundaries specify what each agent is and is not authorized to do. They are separate from the agent's design contract — they are the organizational authorization layer.

---

### Boundary Framework

Every agent at [DemoOrg] is classified by:

1. **Domain** — The business area the agent operates in
2. **Action tier** — The level of consequence of its actions
3. **Autonomy level** — How much the agent can do without human review

#### Action Tiers

| Tier | Action Type | Human Review Requirement |
|------|-------------|--------------------------|
| 1 | Read and summarize | Optional — agent output is advisory |
| 2 | Draft and recommend | Required — human must review before use |
| 3 | Take action in a system | Required — human must approve before execution |
| 4 | Irreversible or high-stakes action | Mandatory — explicit sign-off required |

---

### Deployed Agent Boundaries

#### PM Status Assistant

| Boundary | Definition |
|----------|------------|
| **Domain** | Project Management |
| **Action tier** | Tier 2 — Drafts and recommends |
| **Autonomy level** | Generates report; PMO Lead reviews before distribution |
| **Authorized data sources** | Planner (read only), SharePoint project folder (read only) |
| **Authorized outputs** | Status report document in PMO shared folder |
| **Not authorized** | Send to leadership, update Planner, change project status |

---

#### Editorial Review Assistant

| Boundary | Definition |
|----------|------------|
| **Domain** | Content and Editorial |
| **Action tier** | Tier 2 — Drafts and recommends |
| **Autonomy level** | Generates annotated review; author and editor review |
| **Authorized data sources** | Editorial style guide (read), brand guidelines (read), submitted draft (read) |
| **Authorized outputs** | Annotated review document in review queue |
| **Not authorized** | Approve content, publish, rewrite without instruction |

---

#### M365 Activity Watcher

| Boundary | Definition |
|----------|------------|
| **Domain** | IT Operations |
| **Action tier** | Tier 1 — Read and summarize |
| **Autonomy level** | Fully automated — IT Operations reviews digest |
| **Authorized data sources** | M365 aggregate usage reports via Graph API (read only) |
| **Authorized outputs** | Weekly digest in IT Operations Teams channel |
| **Not authorized** | Access message content, identify individuals, act on accounts |

---

### Global Boundaries (All Agents)

Regardless of tier or domain, **no agent at [DemoOrg] is authorized to**:

- Send external communications without Engagement Lead review
- Approve financial transactions or commitments
- Access data outside its defined knowledge sources
- Operate outside business hours without explicit scheduling authorization
- Store or transmit client data outside authorized systems

---

### Boundary Exceptions

Any request for an agent to act outside its defined boundaries must be:

1. Submitted to the IT Operations Lead in writing
2. Reviewed by the agent's owner
3. Approved by the Operations Director for Tier 3+ actions
4. Documented as a boundary update before the agent acts

Informal "just this once" exceptions are not permitted.
