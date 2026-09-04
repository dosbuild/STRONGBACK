# Failure-pattern checklist — four operator-facing tests

The canonical failure registry is [`docs/ENGINE.md`](../docs/ENGINE.md) §3.
These four are the modes an operator cannot see from inside; each test
replaces introspection with an observation. Run them monthly against your
last two weeks of real work — not against your intentions. A fifth mode —
the host performing a gate fluently — is caught at the artifact level, not
here: read the constraint lists and named error mechanisms (RUN, ATTACK).

**1. Fluent narrative mistaken for structure.**
Smell: you talk about the constraints beautifully.
Test: mutate the surface — rename every domain term, re-skin the problem
into a neighboring field — and re-derive your analysis. If it doesn't
survive renaming, it was vocabulary, not structure.

**2. System performance attributed to self.**
Smell: "I've gotten sharper these last months."
Test: this week's bare run (`weekly-transfer.md`, Test 2). If bare
performance sits at your old baseline, the system improved and you're its
operator — a fine thing to be, as long as the attribution stays straight.

**3. Domain libraries mistaken for transfer.**
Smell: strong results in the domains you usually work in.
Test: the cold-domain run (Test 1). Dropping to baseline in a cold domain
means the gains are local inventories, not a portable operation.
Not failure — inventory. Just don't call it transfer.

**4. Process without judgment.**
Smell: every gate runs, every verdict gets accepted; the checklist is
green and you can't remember disagreeing with the system.
Test: pull one ambiguous ATTACK result from the last two weeks. Without
the model, state which side you'd take and why. If you can't, the gates
ran but the operator did not make a judgment.
