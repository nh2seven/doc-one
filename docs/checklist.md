# Component Checklist

Tracks every major component across three separate questions. Update this as work happens — it's a living doc, not a one-time snapshot.

- **Design** — did we deliberate on this enough? Are the doc's open questions resolved, with no unresolved "TBD"/"recommendation, not decision" language left for MVP scope?
- **Build** — did we build it properly? Code exists implementing the documented contract, matches the documented schema, passes lint/type-check.
- **Test** — did we test it properly? Automated tests cover the component's schema boundaries and the specific failure modes named in its doc, including any [invariant](architecture/platform/invariants.md) it's responsible for.

| Component   | Design         | Build         | Test         | Doc                               |
| ----------- | -------------- | ------------- | ------------ | --------------------------------- |
| <component> | <design state> | <build state> | <test state> | <link to its `architecture/` doc> |

## Currently open design questions

- <the question, and which component's doc it belongs under>
