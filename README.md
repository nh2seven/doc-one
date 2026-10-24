# doc-one

Repository template for a docs-first approach. Docs are the source of truth: code conforms to them, not the other way round.

Start at [docs/\_index.md](docs/_index.md).

## What's here

| Path                 | What it is                                                                                                  |
| -------------------- | ----------------------------------------------------------------------------------------------------------- |
| `AGENTS.md`          | Repo-root guide loaded every agent session — project overview, the one non-negotiable rule, conventions     |
| `docs/_index.md`     | Docs entry point. Every subdirectory has its own `_index.md` — navigation is index-hopping, not a flat tree |
| `docs/architecture/` | Design docs: `pipeline/` (stage flow), `platform/` (cross-cutting), `roadmap/` (deferred)                   |
| `docs/checklist.md`  | Per-component Design / Build / Test tracking — living doc                                                   |
| `docs/research/`     | Facts collected before decisions — candidates, alternatives, licenses. No decisions live here               |
| `docs/runbooks/`     | One runbook per major component, including infra — how to run/inspect it, failure modes                     |
| `docs/references/`   | External links only, never inlined into architecture docs. **Human-clicked only**                           |
| `docs/diagrams/`     | Mermaid source only (`.mmd`), each linked from the doc section it illustrates                               |
| `docs/archive/`      | Superseded docs, kept for history                                                                           |

## Using this template

1. Fill the `<placeholders>` in `AGENTS.md` and `docs/_index.md`: the repo's one-line scope, and **The Rule** — the single non-negotiable engineering constraint the whole design obeys.
2. Write `docs/architecture/principles.md` and seed `docs/architecture/platform/invariants.md`. Invariants follow the law of that doc: each one lands with a test or lint check that enforces it, in the same change.
3. Add one architecture doc per component under `docs/architecture/`, its runbook in `docs/runbooks/`, and its row in `docs/checklist.md` — all three land together, no exceptions.
4. Keep the `references/` warning intact: nothing under `docs/references/` is ever fetched or browsed autonomously.
