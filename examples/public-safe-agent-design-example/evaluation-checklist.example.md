# Evaluation Checklist — Example

> **This is a public-safe illustrative example.** It demonstrates how to evaluate an agent design before deployment and during ongoing governance reviews.

---

## Agent Evaluation Checklist

Use this checklist when:

- Approving a new agent for deployment
- Conducting a quarterly governance review
- Investigating an incident or unexpected output
- Deciding whether to expand an agent's scope

---

## Part 1: Design Completeness

Before any agent is deployed, the design must be complete.

### Contract Completeness

- [ ] Agent has a unique name and identifier
- [ ] A named human owner is assigned
- [ ] Purpose statement is clear and specific (one sentence)
- [ ] Scope is explicitly defined (in scope AND out of scope)
- [ ] Knowledge sources are listed and confirmed accessible
- [ ] Input format and trigger type are defined
- [ ] Output format and destination are defined
- [ ] Escalation rules are specific and testable
- [ ] Constraints are explicit
- [ ] Governance fields are complete (authorization date, review schedule)

### Knowledge Readiness

- [ ] All listed knowledge sources exist and are current
- [ ] Knowledge sources have named owners
- [ ] Update frequency is defined and being followed
- [ ] Knowledge sources are accessible to the agent (permissions confirmed)

---

## Part 2: Pre-Deployment Testing

Before go-live, the agent should be tested against these criteria.

### Functional Testing

- [ ] Agent produces correct output for standard inputs
- [ ] Agent handles missing or incomplete inputs gracefully
- [ ] Agent flags escalation scenarios correctly (does not silently omit)
- [ ] Agent respects all defined constraints
- [ ] Output format matches the defined standard

### Edge Case Testing

- [ ] Agent handles ambiguous inputs without fabricating details
- [ ] Agent correctly identifies out-of-scope requests
- [ ] Agent escalates when confidence is low
- [ ] Agent does not produce outputs that violate organizational principles

### Security and Privacy

- [ ] Agent only accesses its authorized knowledge sources
- [ ] Agent does not expose confidential data in outputs
- [ ] Agent does not retain input data beyond the current session (if required)
- [ ] Access controls on knowledge sources are verified

---

## Part 3: Governance Review (Quarterly)

For ongoing governance reviews of deployed agents.

### Performance

- [ ] Output quality is consistently meeting the defined standard
- [ ] Escalation rate is within expected range (neither too high nor too low)
- [ ] Human reviewers report the agent is saving time and producing useful outputs
- [ ] No incidents or errors reported since last review

### Knowledge Currency

- [ ] All knowledge sources have been reviewed and updated on schedule
- [ ] No knowledge gaps have been identified during operation
- [ ] Knowledge source owners are still active and responsible

### Scope Integrity

- [ ] Agent has not accumulated scope beyond its defined boundaries
- [ ] No ad-hoc extensions have been applied without documented authorization
- [ ] Out-of-scope requests are being correctly handled (escalated or declined)

### Governance Hygiene

- [ ] Audit logs are being maintained as required
- [ ] Owner is still active and accountable
- [ ] Review schedule is being followed
- [ ] No open incidents requiring remediation

---

## Part 4: Incident Response Evaluation

If an incident has occurred (unexpected output, data issue, scope violation):

- [ ] Incident documented with date, description, and impact
- [ ] Root cause identified (knowledge gap / prompt failure / scope violation / model change)
- [ ] Remediation action defined and assigned
- [ ] Agent suspended if risk is ongoing
- [ ] Governance review date moved up (do not wait for scheduled review)
- [ ] Lessons learned captured

---

## Scoring Guidance

There is no pass/fail score. Each unchecked item is a risk to be resolved before deployment (Parts 1–2) or before the next review cycle (Parts 3–4). No agent should be deployed with incomplete Parts 1–2.
