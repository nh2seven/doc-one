# Architecture

**Read [principles.md](principles.md) first.** Every doc below it assumes it: <compress the project's design posture into one sentence — e.g. "every stage is schema-backed, and components are swappable where real alternatives exist and fixed where they don't.">

Then, in whatever order matches what you're touching:

| File                                      | What it is                                                                                              |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [pipeline/\_index.md](pipeline/_index.md) | The target processing flow — one doc per stage                                                          |
| [platform/\_index.md](platform/_index.md) | Cross-cutting concerns every stage relies on: invariants, storage, versioning, the concrete data models |
| [roadmap/\_index.md](roadmap/_index.md)   | Deferred work, kept as design notes so the schema leaves room for it                                    |
