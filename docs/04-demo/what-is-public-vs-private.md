# What Is Public vs. Private

## The Core Distinction

This framework exists in two forms simultaneously:

| Form | What It Contains | Who Can See It |
|------|-----------------|---------------|
| **Public (this repo)** | Principles, patterns, structures, generic examples | Anyone |
| **Private implementation** | Live configurations, business rules, actual knowledge, system integrations | Internal teams only |

Neither form is the "full" system. They serve different purposes.

---

## What Is Public (and Why)

The following content is safe and appropriate for public sharing:

### Principles
The foundational beliefs that guide the architecture. These are generalizable — any organization can evaluate whether they apply.

### Framework layers
The structural model (knowledge → governance → generation → execution). This is an architectural pattern, not a system-specific configuration.

### Agent design patterns
The contract structure, template, and illustrative examples. These show *how* to design an agent without exposing *what* any real agent actually does.

### Generic examples
Fictional organizations, placeholder names, and illustrative data. These demonstrate patterns without revealing specifics.

### Diagrams
Visual representations of structures and relationships. No operational data.

### Public-safe screenshots
Structural views of the live implementation — site organization, folder structure, agent names, and an agent answering a generic query. These show *that the pattern works* without exposing knowledge content, prompts, or configuration. The demo screenshots in [`Screenshots/`](Screenshots/) are an example.

---

## What Is Private (and Why)

The following content belongs in a private implementation only:

### Actual organizational knowledge
- Real business rules and decision criteria
- Internal processes with specific names and steps
- Actual product, client, or pricing information

**Why private:** This is the competitive and operational core of the organization. Exposing it creates both business and security risk.

### Live agent configurations
- Production prompts with organizational context
- Real knowledge source references
- Active integration configurations

**Why private:** These are operational system components. Exposing them could enable manipulation or misuse.

### System integration details
- API keys, tenant IDs, connector configurations
- Internal tool names and URL structures
- Security and access control setup

**Why private:** These are attack surfaces. They must never be public.

### Specific organizational context
- Team structure, personnel, responsibilities
- Current strategic priorities and constraints
- Confidential decisions or rationale

**Why private:** This is internal operational information, not a generalizable pattern.

---

## The Test

When deciding whether something belongs in the public repo, ask:

1. **Could a competitor gain advantage from this?** → Private
2. **Could an attacker exploit this?** → Private
3. **Is this specific to one organization's context?** → Private
4. **Could any organization adapt this for their use?** → Public candidate
5. **Does this illustrate a pattern without revealing specifics?** → Public candidate

---

## Why This Boundary Enables the Framework

If everything were private, the framework would have no value to others. If everything were public, the organization would be exposed. The boundary is the design.

The public framework is valuable *because* it is thoughtfully incomplete. It gives others the structure to build their own private implementation.
