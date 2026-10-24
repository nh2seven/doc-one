# Pipeline

The target processing flow, not a claim that every stage runs today. Read [../principles.md](../principles.md) first. <One sentence on the current state: what's implemented, what's unbuilt.>

Diagram: add one whole-flow Mermaid overview in `../../diagrams/` and link it here — each stage doc then links its own diagram at the specific section it illustrates.

Each stage of the flow gets exactly one doc in this directory, listed in the table below. A new stage doc lands with its [checklist](../../checklist.md) row and its [runbook](../../runbooks/_index.md) file in the same change.

| File         | What it is                                             |
| ------------ | ------------------------------------------------------ |
| `<stage>.md` | <one line: what crosses this stage's boundary, in/out> |

Exact field names and the concrete schemas shared across stages live in the platform doc set — see [../platform/\_index.md](../platform/_index.md).
