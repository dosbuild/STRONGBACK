# CLOSE — close on the written condition

**The problem.** Holding a question open has two failure modes. Snap-closed:
take the first coherent answer. Stuck-open: keep testing after the tests stopped
adding information.

**The rule.** The question closes when the written stop condition is met. If
new information reveals a material risk or a bad frame, revise the stop
condition before continuing and record the change. After planned tests finish,
do not continue research unless the next step names the new uncertainty it will
remove. Log the close in [`state/decisions.log`](../state/decisions.log):
decision · why · what changed · next step · revisit condition.

**Skipped, it fails as:** a fast wrong call or a slow unmade one.
Snap-closers ship the first frame that cohered; stuck-opens convert
judgment into research and file the delay under diligence.

**Failure pattern** *(canon: [`ENGINE`](../docs/ENGINE.md) §3 — compliance
theater)*. Closes without deltas, or open decisions whose next step does not
name a new uncertainty.
**The test:** three consecutive close entries with no "what changed" line, or
any decision still open past its written stop condition with nothing new since.
Either one means the gate has become ritual compliance.

**Engine line.** Closing is a decision rule: finish the planned tests, revise
the plan when evidence requires it, then commit. This gate's hardest boundary —
its own collapse is invisible from inside — lives in ENGINE §5 and is why the
bare test exists. → [`docs/ENGINE.md`](../docs/ENGINE.md)
