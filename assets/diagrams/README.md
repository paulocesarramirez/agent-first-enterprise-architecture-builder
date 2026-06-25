# assets/diagrams/

Rendered/exported versions of the framework diagrams, for use in presentations, slides, and external documentation where Mermaid cannot render natively.

## Available diagrams

| File | Description | Mermaid source |
|------|-------------|----------------|
| [`architecture-layers.svg`](architecture-layers.svg) | The four-layer architectural model (Knowledge → Governance → Generation → Execution) | [`examples/diagrams/architecture-layers.mmd`](../../examples/diagrams/architecture-layers.mmd) |
| [`knowledge-to-execution.svg`](knowledge-to-execution.svg) | How knowledge flows through governance and generation into execution | [`examples/diagrams/knowledge-to-execution.mmd`](../../examples/diagrams/knowledge-to-execution.mmd) |
| [`public-private-boundary.svg`](public-private-boundary.svg) | The boundary between public-safe content and private implementation | [`examples/diagrams/public-private-boundary.mmd`](../../examples/diagrams/public-private-boundary.mmd) |

## Conventions

- **Source of truth** for every diagram is the Mermaid (`.mmd`) file in [`examples/diagrams/`](../../examples/diagrams/). Edit the `.mmd` first, then re-export here.
- Rendered files keep the **same base filename** as their source, with an image extension (`.svg` preferred, `.png` acceptable).
- Prefer `.svg` for crisp scaling in docs and slides; add a `.png` variant only when a tool cannot consume SVG.
- Keep diagrams public-safe — no proprietary data, credentials, or confidential business logic.

## How to re-export

1. Update the source `.mmd` file in `examples/diagrams/`.
2. Render it (Mermaid CLI, the [Mermaid Live Editor](https://mermaid.live/), or the VS Code Mermaid extension).
3. Export to this folder using the matching base filename.
4. If you add a new diagram, list it in the table above and in [`docs/04-demo/screenshots-and-diagrams.md`](../../docs/04-demo/screenshots-and-diagrams.md).
