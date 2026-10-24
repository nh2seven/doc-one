# Platform

Cross-cutting concerns every stage relies on or must respect — not a stage you pass through, but infrastructure and policy the stages sit on top of.

| File                           | What it is                                                                                              |
| ------------------------------ | ------------------------------------------------------------------------------------------------------- |
| [invariants.md](invariants.md) | The concrete, enforceable rules distilled from every doc here. Read this to know what must never break. |

Beyond that, one doc per cross-cutting concern as it lands — the usual set: `data-models.md` (the concrete schemas — read this when you need exact field names/types), `storage.md`, `versioning.md`, plus any policy docs (privacy/consent, external/validation data) the project earns.
