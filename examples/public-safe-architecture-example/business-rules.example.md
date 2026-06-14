# Business Rules — Example

> **This is a public-safe illustrative example.** All organization names, rules, and context are fictional. This demonstrates how an organization might document business rules for agent consumption.

---

## [DemoOrg] — Business Rules Reference

*Version 2.0 | Owned by: [Operations Director] | Reviewed: Quarterly*

---

### Purpose

This document contains the business rules that govern decisions made at [DemoOrg]. It is the authoritative reference for any agent that needs to apply organizational decision logic.

---

### Communication Rules

| Rule ID | Rule | Authority |
|---------|------|-----------|
| COM-01 | All external client communications must be reviewed by the Engagement Lead before sending | Operations Director |
| COM-02 | Responses to client queries must be acknowledged within 4 business hours | Client Operations |
| COM-03 | Substantive responses to client queries must be delivered within 1 business day or a timeline committed | Engagement Lead |
| COM-04 | No pricing discussions may occur without the Commercial Lead present or explicitly authorized | Commercial Director |

**Agent application:** Agents that draft communications must flag any draft that involves pricing, scope changes, or client escalations for human review before sending.

---

### Approval Thresholds

| Decision Type | Approval Required From | Threshold |
|--------------|----------------------|-----------|
| Scope addition | Engagement Lead | Any scope change |
| Budget variance | Operations Director | > 10% of engagement value |
| Discount authorization | Commercial Director | Any discount |
| New vendor engagement | Operations Director | > [threshold amount] |
| Emergency resource allocation | Delivery Director | Any emergency |

**Agent application:** Agents must never approve, commit to, or communicate any decision that falls within these approval thresholds. They must escalate.

---

### Escalation Rules

#### When to Escalate Immediately

- A client expresses serious dissatisfaction or threatens to terminate
- A deliverable will be late by more than 2 business days
- A team member identifies a material error in previously delivered work
- A conflict of interest is identified

#### Escalation Path

```
Issue identified
    │
    ▼
Engagement Lead notified (immediate)
    │
    ▼
Operations Director notified (within 2 hours for urgent issues)
    │
    ▼
[Executive Sponsor] notified (if client relationship at risk)
```

---

### Quality Standards

| Standard | Rule |
|----------|------|
| All deliverables reviewed by at least one person other than the author before client delivery |
| All client-facing documents use the approved [DemoOrg] template |
| Meeting notes distributed within 24 hours of any client meeting |
| All open actions tracked in the engagement Planner board |

---

### Confidentiality Rules

| Rule | Description |
|------|-------------|
| Client data isolation | Information from one client engagement must never be used in another engagement without explicit written consent |
| Document sharing | Client documents must not be shared outside the engagement team SharePoint without Operations Director approval |
| Public reference | Client names may not be used in public references or case studies without written consent |

**Agent application:** Agents must not reference or retrieve data from one client's knowledge base when assisting with another client's work.

---

*These rules are mandatory. Agents must apply them consistently and escalate when a situation is ambiguous rather than making an exception.*
