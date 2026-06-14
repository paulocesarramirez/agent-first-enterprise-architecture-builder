# Public Repo Boundary

## Why this document exists

This repository is public.

That creates an important architectural and governance requirement:

The repository must share the **public architecture, framework, and reference patterns** of the project without exposing the private operational implementation used in the live EmprendHEC environment.

This document defines that boundary.

---

## Core rule

> **Publish the architecture. Keep the operations private.**

This repository is intended to share:
- the framework
- the architecture
- the mindset
- the governance principles
- the public reference patterns
- the reusable scaffolding

It is **not** intended to publish:
- confidential operational logic
- private execution details
- client or customer data
- sensitive internal prompts
- private knowledge bases
- production-ready internal business artifacts

---

## Public layer

The **public layer** may include:

- architecture definitions
- governance principles
- source-of-truth concepts
- human-centered design principles
- reusable design patterns
- public-safe examples
- templates
- placeholder agent designs
- public-safe diagrams
- generic documentation structures

This is the layer intended for learning, adoption, adaptation, and open discussion.

---

## Private layer

The **private layer** includes material that must remain outside this repository.

Examples include:

- internal prompts used by the working EmprendHEC system
- internal execution rules tied to real business operations
- operational report formats
- live knowledge-base content
- customer or client content
- credentials, secrets, tokens, or private endpoints
- private process details not approved for public release
- screenshots or exports containing sensitive business data

This private layer may be demonstrated in controlled contexts such as the live demo, but it should not be committed to this repository.

---

## Why the boundary matters

A public repository must support:
- transparency
- learning
- reproducibility
- open collaboration

But a real operating system also contains:
- confidential organizational logic
- competitive execution details
- business-sensitive materials
- operational assets that require governance

If these two layers are mixed, the result is:
- avoidable risk
- weak security
- architectural confusion
- poor governance

A clean boundary makes the project stronger, not weaker.

---

## Public examples are not production exports

Examples in this repository must always be:

- abstracted
- genericized
- public-safe
- clearly labeled as examples, placeholders, or templates

They should illustrate the framework, not expose the private working implementation.

This applies especially to:
- agent design examples
- prompt structures
- workflow templates
- architecture diagrams
- implementation guidance

---

## Boundary test

Before adding any file, ask:

### 1. Is this content safe for worldwide public access?
If no, do not commit it.

### 2. Does this file teach the architecture without exposing private operations?
If no, rewrite it as a public-safe abstraction.

### 3. Would publishing this weaken business security, confidentiality, or governance?
If yes, keep it private.

### 4. Is this an example, a template, or a real production export?
If it is a production export, it probably does not belong here.

---

## Practical rule for contributors

When information is useful conceptually but unsafe operationally:

- do not omit the idea
- do not expose the real implementation
- create a public-safe placeholder or template instead

Examples:
- instead of a real private prompt → publish a prompt template
- instead of a real private workflow → publish an abstract workflow pattern
- instead of a real internal knowledge base → publish a knowledge base structure example

---

## Relationship to the live demo

The live demo validates that the framework works in a real environment.

That does **not** mean the real environment should be open-sourced.

The repository and the demo play different roles:

- **repository** → public architecture and public-safe patterns
- **demo** → proof that the framework already works in practice

This separation is intentional and healthy.

---

## Final principle

The repository should make the framework understandable, reproducible, and inspiring.

It should not expose confidential operations.

> Share the pattern.  
> Protect the implementation.
