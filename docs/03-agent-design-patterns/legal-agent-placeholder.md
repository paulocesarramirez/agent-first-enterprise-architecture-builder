# Legal Agent — Placeholder

> This agent design is planned but not yet documented. This placeholder reserves the space and outlines the intended scope.

---

## Intended Purpose

The Legal Agent is designed to support legal and compliance teams by assisting with routine review tasks, flagging potential compliance concerns, and maintaining a structured view of legal obligations and deadlines.

## Planned Capabilities

- Reviewing documents against defined compliance checklists
- Flagging clauses or terms that deviate from standard positions
- Tracking regulatory deadlines and obligations
- Summarizing legal documents for non-legal stakeholders (with appropriate caveats)

## Design Considerations

This agent operates in an extremely high-consequence domain. Key constraints include:

- **Not legal advice** — All agent outputs must be clearly framed as analytical support, not legal opinion
- Qualified legal review is required for all outputs used in decision-making
- The agent must never draft binding legal language autonomously
- Privacy and confidentiality protections are paramount — access controls are critical
- Regulatory differences across jurisdictions must be explicitly accounted for in scope

## Status

- [ ] Agent contract drafted
- [ ] Knowledge sources identified
- [ ] Governance requirements defined
- [ ] Legal owner assigned
- [ ] Compliance review completed
- [ ] Approved for design

## Related Examples

- [`editorial-agent-example.md`](editorial-agent-example.md) — Review-oriented agent pattern
- [`common-agent-contract.md`](common-agent-contract.md) — Template to complete when ready

---

> To contribute this agent design, follow the process in [`CONTRIBUTING.md`](../../CONTRIBUTING.md) and use [`public-agent-template.md`](public-agent-template.md).
