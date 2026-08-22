# Sparks — raw candidates.

# Each one graduates into its own file once it survives the test:

# is there a concrete recurring scene — not just a general truth?

1. Loading/skeleton states get designed last, if at all — in interactive, dynamic UI, transitional states are treated as "obviously how it should look" rather than an actual decision, so they're the first thing dropped when time or budget runs out.

2. Extending UI on an existing but undocumented system defaults decisions to the engineer's memory of other pages — "consistency" ends up maintained informally by whoever is implementing, not by a documented rule anyone else can follow.

3. A long, multi-step data-collection flow with no way to save progress at intermediate points loses users to interruption (time, attention, connectivity) — resulting in everything entered beign lost.

4. Features get built as isolated sections (with their own data and screen) before the product needs them interconnected — once the same underlying data needs to surface across sections that were never designed to reference each other, which becomes technical debt instead of a planned relationship.

5. Presenting AI-generation customization options as freely combinable, when some combinations don't have enough underlying data or context to generate well, produces failed or low-quality output — the fix is making later options conditional on earlier choices, not exposing the full option space upfront.

6. Unbounded AI output length swings unpredictably between too short and too long — without an explicit limit and user control over scope, perceived reliability drops even when the content itself is accurate.
