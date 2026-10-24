# AGENTS.md — <Project Name>

> Repo-root guide, loaded automatically every session here. This repo is <one sentence: what it owns, end to end — the intake-to-output boundary this repo is responsible for>. Start at [docs/\_index.md](docs/_index.md).

## Project Overview

<2–4 sentences or bullets: what the project is, who it serves, the one-line shape of the system.>

- **Tagline:** <optional>

## The Rule

> **<The single non-negotiable engineering constraint, one imperative sentence.>**

<One short paragraph: why it exists and what it overrides — convenience, speed, "just this once". This is the one non-negotiable engineering constraint for anything touching the system; every answer below its confidence threshold is parked for human review, and the human's decision is final.>

A close second, if the project has one: <secondary constraint, e.g. "everything is schema-backed; components are swappable where real alternatives exist and fixed where they don't." See docs/architecture/principles.md.>

## Invariants

Concrete, enforceable rules distilled from every doc in `docs/architecture/` — not guidelines, and not optional. A new invariant lands with a test or lint check that enforces it, in the same change; otherwise it's a pitfall note, not an invariant. Full list: [docs/architecture/platform/invariants.md](docs/architecture/platform/invariants.md).

## Coding & Documentation Conventions

- **Docstrings and comments stay terse and objective** — state what a thing exists for, nothing else. No subjective language, no future maybes, no justifications, no "parked for later" narration.
- **A decision lives in its doc, once.** A comment referring to a decision names the doc it lives in (e.g. "see docs/architecture/platform/data-models.md"), never restates the reasoning inline.
- **Docs never reference code** — no file paths, module names, or "see this class's docstring." Docs are the source of truth; code conforms to them, not the other way round. A doc quoting an exact required pattern as a normative invariant (e.g. a config shape in an invariants doc) is prescribing behavior, not pointing at a location — that's not the same thing as naming a file to go look at.
- **Docs stay current.** Drift caught while doing unrelated work gets fixed immediately, not filed away for later.
- **Re-sync the lockfile after every dependency-manifest change**, so the lockfile never drifts from what's declared.
- **Tests cover failure modes exhaustively, not just the happy path.** For every new schema or function, work backwards from "what are all the ways this can be given bad input" before considering the test suite done.
- **Segregate docs just enough, not more.** A new doc is warranted when a concern doesn't fit its most obvious existing home without diluting that doc's own scope. Don't spin up a new file for something that's one paragraph inside an existing doc, and don't keep bolting unrelated concerns onto a doc that already has a clear, narrow scope.
- **Don't run tests until the user explicitly signs off.** Mid-build test runs are noise, not signal, when a piece of work isn't at its final iteration yet. Build the whole thing, run the suite once at the end, and treat whatever breaks as the feedback loop for finishing touches — not a running commentary during the build.

## Start Here

<One paragraph: what has actually landed — foundation pieces, shared contracts, verifiers — and what remains unbuilt, so nobody infers a running full system from the design docs.> Before proposing any pipeline or architecture work:

1. Read [docs/\_index.md](docs/_index.md), then [docs/architecture/principles.md](docs/architecture/principles.md).
2. Read the doc for the area you're touching — follow the index chain: `docs/_index.md` → `docs/architecture/_index.md` → `pipeline/_index.md` / `platform/_index.md` / `roadmap/_index.md`.
3. Re-check this file — it will grow sections (directory layout, coding conventions) as more code lands. Don't invent those sections ahead of the code that would justify them.

## Documentation

Docs are navigated by index-hopping, not a flat table: `docs/_index.md` is the entry point, and every subdirectory has its own `_index.md` pointing further in. Don't link directly to a deep doc from here — start at the index and follow it.

| Path                 | What's there                                                                                                                            |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `docs/_index.md`     | Entry point                                                                                                                             |
| `docs/architecture/` | Design docs: `pipeline/` (stage flow), `platform/` (cross-cutting: storage, versioning, data models, invariants), `roadmap/` (deferred) |
| `docs/checklist.md`  | Per-component design/build/test tracking — update it as work happens                                                                    |
| `docs/research/`     | Facts collected before decisions — candidate techniques, models, codebases, licenses — plus the decisions made during it                |
| `docs/diagrams/`     | Mermaid source only (`.mmd`), nothing else. See below                                                                                   |
| `docs/runbooks/`     | One runbook per major component (pipeline + platform + infra) — how to run/inspect it, mock payloads, failure modes                     |
| `docs/references/`   | External links only: related repos, papers, model cards, third-party docs                                                               |
| `docs/archive/`      | Superseded docs, kept for history                                                                                                       |

**Diagrams.** When a doc describes a flow, a state machine, or how data models relate, that explanation gets a Mermaid diagram in `docs/diagrams/` (one `.mmd` file, Mermaid syntax only — no other diagram format), linked from the doc at the specific section it illustrates, not just dumped at the top of the file. If you change the thing a diagram describes, update the diagram in the same change — a stale diagram is worse than no diagram.

**Runbooks.** Every component documented in `docs/architecture/` gets a runbook in `docs/runbooks/`, no exceptions — including a component that isn't independently interactable (it still gets one, even if "how to run it" is just config inspection) and infra the project depends on (databases, emulators, container stacks). A new component doc and its runbook land together.

**References.** Anything outside this repo — another repo, a paper, a model card, third-party docs — is a link in `docs/references/`, never inlined into an architecture doc. Repo links are discovered on disk (a sibling directory next to this repo) or by asking the user to clone them — never a hardcoded local path. **No link under `docs/references/` is ever fetched or browsed autonomously**, including the open-internet ones — it's there for a human to open.

## MCP Servers

<Optional. If infra MCP servers (Docker, database, ...) are registered for this project, state which ones, what they point at, and route reads/writes for that infra through the registered tools, not raw shell commands. Their setup steps live in their own repos' READMEs / AGENTS.md — don't duplicate them into this file.>
