# ATTACK — nothing ships unverified

**The problem.** The model can be fluent when it is wrong. A persuasive answer
is not evidence that the process could catch its own mistake.

**The rule.** Before anything ships, the model attacks its own result:
strongest counter-case, most likely failure mechanism. Then it checks the
attack. A check counts only if it names a plausible error in the original
process that the check could expose. A different source, method, tool, model,
dataset, or frame can help, but does not prove independence. Name the error
being tested, how the check's mechanism differs, and which blind spots remain
shared.

**Skipped, it fails as:** confident wrongness at scale — worse than visible
uncertainty, because it triggers no review in the people downstream.

**Failure pattern** *(canon: [`ENGINE`](../docs/ENGINE.md) §3 — compliance
theater; surface compliance)*. Attack theater: a self-critique that never
changes a verdict. A fluent host performs this gate as convincingly as it
performs answers, so what you read is the named error mechanism, not the
thoroughness of the prose. Re-reading and rephrasing do not count as checks.
**The test:** count the attacks in the last month that changed a decision.
Zero means the checks are not applying pressure, or the task mix is too safe.

**Engine line.** Independence is about error mechanisms, not labels on tools.
→ [`docs/ENGINE.md`](../docs/ENGINE.md)
