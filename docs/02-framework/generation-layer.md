# Generation Layer

## Purpose

The Generation Layer is where AI models are applied to produce **useful outputs** — drafts, summaries, recommendations, analyses, and structured responses — grounded in the knowledge layer and constrained by the governance layer.

This is the layer most people think of when they think of "using AI." In this framework, it is deliberately placed third — because generation without knowledge and governance produces fluent but unreliable outputs.

## What Generation Covers

| Output Type | Examples |
|-------------|----------|
| **Drafting** | Emails, reports, proposals, documentation |
| **Summarization** | Meeting notes, document digests, status summaries |
| **Analysis** | Risk assessments, gap analysis, comparisons |
| **Recommendations** | Next steps, prioritization, decision support |
| **Structured extraction** | Pulling key data from unstructured content |
| **Transformation** | Reformatting content for different audiences or systems |

## Design Principles for Generation

### Ground outputs in Layer 1

Every generation task should specify:

- What knowledge sources the agent should consult
- What the authoritative reference is for factual claims
- What to do when relevant knowledge is missing

### Respect Layer 2 boundaries

Generation must not:

- Produce outputs that exceed the agent's authorized scope
- Make decisions that require human judgment
- Present uncertain outputs as certain

### Design for evaluation

Every generated output should be:

- Reviewable by a human before acting on it
- Structured so its quality can be assessed
- Traceable to its inputs and instructions

## Prompt Architecture

Effective generation depends on intentional prompt design. Each agent prompt should include:

1. **Role definition** — What the agent is and what it does
2. **Knowledge grounding** — What sources to consult
3. **Task description** — What is being asked
4. **Output format** — How the response should be structured
5. **Constraints** — What the agent must not do or say
6. **Escalation trigger** — When to stop and ask for human input

See [`docs/03-agent-design-patterns/common-agent-contract.md`](../03-agent-design-patterns/common-agent-contract.md) for the standard structure.

## Model Selection

The generation layer does not prescribe a specific model. Selection criteria should include:

- Context window requirements (how much knowledge the agent needs to process)
- Output quality requirements for the specific task type
- Cost and latency constraints
- Data residency and privacy requirements

## Related Documents

- [`architecture-layers.md`](architecture-layers.md) — Layer 3 context
- [`knowledge-architecture.md`](knowledge-architecture.md) — The foundation generation depends on
- [`agent-governance-layer.md`](agent-governance-layer.md) — The constraints generation must respect
- [`examples/public-safe-agent-design-example/prompt-structure.example.md`](../../examples/public-safe-agent-design-example/prompt-structure.example.md)
