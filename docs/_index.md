# <Project> Docs

<One paragraph of scope, no marketing voice: what this repo owns end-to-end, what stage of the product it covers, what's implemented vs. unbuilt as of now. The agent reads this to know where the work actually stands.>

Start at [architecture/\_index.md](architecture/_index.md) — that's the design doc set.

| File                                | What it is                                                                                                                                                                             |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [checklist.md](checklist.md)        | Per-component tracking: is the design finalized, is it built, is it tested. Living doc, update it as work happens.                                                                     |
| `architecture/`                     | The design doc set — the target system, not a claim that every part runs today. Entry: [architecture/\_index.md](architecture/_index.md).                                              |
| [research/](research/_index.md)     | Facts collected before decisions — candidate techniques, models, codebases, datasets, licenses. No decisions; the architecture docs are unchanged by it.                               |
| `diagrams/`                         | Mermaid source only (`.mmd`). Every diagram is linked from the doc it illustrates, at the relevant section — this directory has no content of its own, only referenced from elsewhere. |
| `runbooks/`                         | One runbook per major component — how to run/inspect it, mock payloads, failure modes. Includes infra.                                                                                 |
| [references/](references/_index.md) | External links: related repos, papers, model cards, third-party docs. **Human-clicked only — see the warning in `references/_index.md`.**                                              |
| `archive/`                          | Superseded docs, kept for history.                                                                                                                                                     |
