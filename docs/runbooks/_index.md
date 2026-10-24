# Runbooks

Operational guidelines on how to run, understand and interpret the project. One runbook per major component — even a component that isn't independently interactable (config consumed by another stage, not a service of its own) still gets one, and deferred/roadmap components get a stub ("Stub — deferred, nothing to run yet"). Infra the project depends on gets one too. This is a living document, updated as the system evolves.

A new architecture doc and its runbook land together.

## Components

| File             | What it is                                                           |
| ---------------- | -------------------------------------------------------------------- |
| `<component>.md` | <how to run/inspect it, mock payloads, state queries, failure modes> |

## Infrastructure

| File         | What it is                                               |
| ------------ | -------------------------------------------------------- |
| `<infra>.md` | <running, connecting to, and resetting the dev instance> |

## External data

| File           | What it is                                                 |
| -------------- | ---------------------------------------------------------- |
| `<dataset>.md` | <how to actually pull it, and what to fix before using it> |
