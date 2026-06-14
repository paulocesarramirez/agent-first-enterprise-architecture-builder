# Safe Scaffolding Instructions

## Purpose

This document tells GitHub Copilot (and any contributor) **how to add new content to this repository safely**. It is the operational companion to the public-safe rule in [`.github/copilot-instructions.md`](../../.github/copilot-instructions.md).

Everything generated here — docs, examples, diagrams, templates, scaffolds — must respect one governing constraint:

> **Public-safe only.** Share the architecture, framework, and patterns. Never share confidential operational detail.

---

## The public-safe rule

**Always:**
- Use only public-safe, generic, non-confidential information.
- Keep agent and organization examples abstracted, genericized, and clearly labeled as examples or placeholders.
- Maintain an explicit boundary between public examples and private implementation.

**Never:**
- Invent or expose internal operational details of EmprendHEC (private prompts, confidential workflows, live decision rules, proprietary data structures) unless explicitly approved for public release.
- Include secrets, credentials, endpoints, tenant IDs, customer/client data, PII, or internal business logic.
- Present illustrative examples as production-ready or export the private working system.

**If an artifact would require confidential information:**
- Do not fabricate or infer it.
- Generate a **public-safe placeholder** and explicitly label the missing content as a private implementation detail.

---

## The quick test (before adding anything)

Ask, in order:

1. **Could a competitor gain advantage from this?** → keep it private.
2. **Could an attacker exploit this?** → keep it private.
3. **Is this specific to one organization's confidential context?** → keep it private.
4. **Could any organization adapt this for their use?** → public candidate.
5. **Does this illustrate a pattern without revealing specifics?** → public candidate.

Full rationale: [../04-demo/what-is-public-vs-private.md](../04-demo/what-is-public-vs-private.md) and [../01-principles/public-repo-boundary.md](../01-principles/public-repo-boundary.md).

---

## Where new content goes

| Artifact | Location | Notes |
|----------|----------|-------|
| New documentation | the matching `docs/0X-` folder | one concept per file |
| New example | `examples/` | filename ends in `.example.md` |
| New diagram | `examples/diagrams/` | Mermaid `.mmd` |
| New starter kit | `starter-kits/` | public-safe scaffolds only |
| Visual assets | `assets/` (or `docs/04-demo/Screenshots/` for demo images) | review every image first |

Follow [naming-conventions.md](naming-conventions.md) for names. Do **not** create files outside the defined structure without discussion. Do **not** modify `docs/01-principles/` without explicit instruction — those are foundational.

---

## Allowed vs. not allowed

**Copilot may generate:**
- markdown documentation, diagrams, and example templates
- placeholder config files and public-safe code scaffolds
- starter kits, generic agent design patterns, and folder structures

**Copilot must not generate:**
- executable code for production deployment
- real prompts, knowledge-base contents, or live configurations
- anything containing secrets or confidential business logic

---

## Using placeholders

When real content would be confidential, substitute clearly-labeled placeholders:

- Organizations: `[YourOrg]`
- Systems: `[YourSystem]`
- Processes: `[YourProcess]`
- Responsibilities/scope: `[single responsibility]`, `[exclusions]`
- Behaviors: `[allowed autonomous behaviors]`, `[disallowed behaviors]`

A reader should be able to drop in their own values without ever seeing private EmprendHEC detail.

---

## Reviewing screenshots and images

Before adding any image, confirm it does **not** reveal:
- real client, customer, or personnel names or PII
- confidential business rules, pricing, or internal decision logic
- private prompts, knowledge-base contents, or system instructions
- secrets, credentials, tenant IDs, endpoints, or connector configuration

If it does, **redact, blur, or recreate it with placeholder data** first. See the screenshot ground rules in [../04-demo/screenshots-and-diagrams.md](../04-demo/screenshots-and-diagrams.md).

---

## Pre-commit checklist

Before saving or committing new content:

- [ ] No secrets, credentials, keys, tokens, tenant IDs, or endpoints.
- [ ] No real client, customer, or personnel data / PII.
- [ ] No confidential prompts, business rules, pricing, or decision logic.
- [ ] Examples are generic and labeled; placeholders used where needed.
- [ ] File is in the correct folder and follows naming conventions.
- [ ] `docs/01-principles/` untouched unless explicitly requested.
- [ ] Cross-references/links are valid.

---

## Related documents

- [naming-conventions.md](naming-conventions.md) — file and folder naming rules
- [repo-implementation-guidelines.md](repo-implementation-guidelines.md) — how others implement the framework
- [../04-demo/what-is-public-vs-private.md](../04-demo/what-is-public-vs-private.md) — the public/private boundary
- [../01-principles/public-repo-boundary.md](../01-principles/public-repo-boundary.md) — the foundational boundary principle
