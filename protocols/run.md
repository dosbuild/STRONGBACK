# RUN — never one pass

**The problem.** One output can hide how much the answer depends on the
operator's framing, and on the decomposition, constraints, order of decisions,
or method the model happened to pick.

**The rule.** When those choices could change the result, the model produces at
least two structurally different passes: a different decomposition, constraint
set, method, or order of decisions. It varies the structure, not the frame —
the frame is yours, fixed at FRAME; a pass that quietly reframes the task is
answering a different one. Each pass ships with its assumed constraints,
listed, so the operator can read the difference: "the passes differ" is a
claim; two lists you can compare are evidence. If the task is deterministic,
mechanical, or already independently checked, the model proposes the narrower
check and why — and skips only on the operator's approval, because "a second
pass adds nothing" is itself a judgment call, and judgment does not delegate.
When two passes run, separate what held across passes from what moved.

**Skipped, it fails as:** shipping the first frame. The answer looks stable
because no other structure was tried.

**Failure pattern** *(canon: [`ENGINE`](../docs/ENGINE.md) §3 — correlated
checks; surface compliance)*. Variation theater: passes that differ in
vocabulary, register, or presentation order while sharing one decomposition
underneath — whether the operator faked it or the host performed it fluently.
**The test:** read the two constraint lists. Missing or matching lists mean
presentation changed, not structure.

**Engine line.** A second structure is useful when it can expose dependence on
the first one. → [`docs/ENGINE.md`](../docs/ENGINE.md)
