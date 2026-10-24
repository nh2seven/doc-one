# Architecture Principles

Status: <phase> — read this before any other doc in this directory.

Every doc in `docs/architecture/` follows these rules. They are not optional per-component preferences; they are the constraints the system is designed under.

## 1. <Principle name>

<One or two paragraphs: the rule itself, then an "In practice:" list showing how it shows up concretely — e.g. every stage declares input/output schemas validated at the boundary, not assumed; nothing is "just a file on disk.">

## 2. <Principle name>

<...and where useful, the decision test the principle implies, stated once so it doesn't get re-argued per component. E.g.: **The test:** if we can name a real second option today, or expect to swap this within a year, it goes behind an interface. Otherwise, pick the standard tool and move on.>

## 3. <Principle name>

<...>
