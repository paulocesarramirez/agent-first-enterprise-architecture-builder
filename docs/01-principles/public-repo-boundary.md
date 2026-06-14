# Public Repo Boundary

## Principle

> This repository is a public-safe representation of the framework. The boundary between what is shared and what is kept private is intentional and principled, not arbitrary.

## The Dual Reality

This framework exists in two forms:

| Form | Contents | Audience |
|------|----------|----------|
| **Public repo** (this repository) | Principles, patterns, generic examples, diagrams | Anyone |
| **Private implementation** | Live agent configurations, business rules, internal knowledge, system integrations | Internal teams only |

The public repo is a **structural and conceptual representation**. The private implementation is the operational reality. Neither is complete without the other — but they serve different purposes.

## What Determines the Boundary

Content belongs in the public repo if it is:

- **Generalizable** — Useful to organizations beyond the one that created it
- **Safe** — Free of proprietary data, credentials, or exploitable detail
- **Principled** — Reflective of architectural thinking, not implementation specifics
- **Illustrative** — Demonstrates a pattern rather than exposing a system

Content stays private if it:

- Contains specific business logic or decision criteria
- Names internal systems, vendors, or integrations
- Could enable unauthorized access or misuse if public
- Represents competitive advantage that should not be disclosed

## The Responsibility of Contribution

Contributors to this public repo must apply this boundary to every contribution. When in doubt, ask:

> "If a competitor read this, would it harm the organization?"

If yes, it does not belong in the public repo.

## Why This Boundary Matters for the Framework

An architectural framework that leaks operational details loses value in two directions:

1. **Security risk** — Exposed configurations can be exploited
2. **Generalizability loss** — Overly specific examples are less useful to others

The boundary preserves both the security of private systems and the utility of the public framework.

## Related Documents

- [`docs/00-overview/public-demo-scope.md`](../00-overview/public-demo-scope.md) — What is and isn't in this repo
- [`docs/04-demo/what-is-public-vs-private.md`](../04-demo/what-is-public-vs-private.md) — Deeper explanation with examples
- [`CONTRIBUTING.md`](../../CONTRIBUTING.md) — Contribution rules that enforce this boundary
