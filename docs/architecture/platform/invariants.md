# Invariants

Status: <phase>. Follows [principles.md](../principles.md).

These are concrete, checkable rules — not guidelines. Each one is distilled from a decision already made elsewhere in `docs/architecture/`; this doc exists so they're in one place instead of scattered across ten files.

**The law of this list:** a new invariant lands with a test (or a lint/schema check) that enforces it, in the same change. If nothing enforces it, it's a preference, not an invariant — don't add it here.

Implementation scope: <which rules actually have enforcing checks today vs. which remain requirements for unbuilt components — keep this honest, see [the checklist](../../checklist.md).>

1. **<Invariant — one checkable sentence about what must never break>.** See [<doc where the decision lives>](path).
2. **<...>** See [<...>](path).
