# ENGINE — the working theory under the file

Nothing here is needed to install the protocol. This file is for judging the
protocol and forking it well: what STRONGBACK assumes, where it fails, who it
serves, and what evidence would move the claim either way.

## 1. Working hypothesis

On complex, deferrable work, result quality tracks two things: the operator's
judgment, and the density of independent checks the process can afford. Read
it as a product, not a sum — weak judgment with many checks still ships
errors, and sharp judgment with no checks still ships blind.

Models move the second term. Alternatives, counter-cases, retrieval,
summaries, test plans, and comparisons get cheaper with each model
generation, so the checking term rises on a curve the operator does not have
to climb. Judgment seems to train slowly; the external term is the one that
compounds. That gap is the reason to install a protocol instead of collecting
techniques — a technique is fixed at the moment you learn it, while a loop
that spends the cheap checking term rides the curve.

The strongest counter-argument, named: the same releases that make checks
cheaper make errors more persuasive. A more capable model is more fluent when
it is wrong, so the difficulty of judging any single answer rises with the
capability that was supposed to help. If the protocol asked the operator to
evaluate answers head-on, the two curves might cancel. The bet is narrower.
The gates never ask for head-on evaluation; they ask the operator to read
artifacts — a constraint list per pass, a named error mechanism per check, a
written stop condition — and artifacts stay legible as fluency rises, because
they are short, comparable, and produced before persuasion attaches to a
conclusion. How much fluent wrongness still leaks through legible artifacts
is an open question (§6). The honest claim: the counter partially offsets the
compounding term; the bet is that it does not cancel it.

Files move a third thing: state. A task card, prediction log, decision log,
and model-of-me cut what the operator must hold in working memory. The
judgment calls stay with the operator: what task matters, what success means,
which checks count, when to stop.

STRONGBACK turns this into a repeatable sequence: FRAME, PREDICT, RUN, ATTACK,
CLOSE. Treat all of it as a working model, not a proven law of intelligence.

## 2. Why these five gates

- **FRAME** prevents fluent work on the wrong task. It records the
  deliverable, success criterion, and stop condition before work starts; on
  tasks that are ambiguous, costly to reverse, likely to expand, public, or
  governed by conflicting criteria, it adds the forbidden outcome, suspected
  bottleneck, cheapest useful test, and hard constraints.
- **PREDICT** prevents post-hoc agreement with the answer. It asks for a
  falsifiable expectation before output: expected result, main factor,
  winning version, direction of change, or probability when the event has
  calibration value.
- **RUN** prevents mistaking one framing for the answer. When a result
  depends on framing, decomposition, constraints, order of decisions, or
  method, it asks for a second structure — each pass's constraints listed —
  and compares what stayed fixed with what moved. Skipping the second pass is
  the operator's call, never the model's.
- **ATTACK** prevents fluent wrongness from shipping unchecked. It names the
  most likely failure mechanism, then checks for a plausible error the
  original process could have missed.
- **CLOSE** prevents both premature acceptance and endless research. It
  closes on the written stop condition, unless new information forces a
  recorded revision before work continues.

Every gate has residual failure modes. They live in one place — §3, the
canonical registry. The per-gate pages in `protocols/` and the checklist in
`evals/` are views of that registry, not separate taxonomies.

## 3. Failure registry (canonical)

When a failure shows up anywhere in this repo — a per-gate page, the
checklist, a log entry — it should resolve to a name here.

- **Compliance theater.** Every gate is performed, no decision changes:
  cards that constrain nothing, attacks that never flip a verdict, closes
  with an empty delta. Operator-facing tests:
  [`evals/failure-pattern-checklist.md`](../evals/failure-pattern-checklist.md).
- **Surface compliance by the host.** The model performs a gate as fluently
  as it performs answers: two "different" passes sharing one decomposition,
  an "attack" that is a summary in adversarial vocabulary. The operator
  cannot cheaply audit compute they delegated — that was the point of
  delegating. Partial defense, built into the gates: each gate must emit a
  legible artifact (a constraint list per pass, a named error mechanism per
  check), and the operator reads the artifact, not the prose. "The passes
  differ" is a claim; two lists you can compare are evidence.
- **Correlated checks.** Several checks — or passes — share the same blind
  spot and produce agreement without pressure. Different tools or sources
  reduce correlation but do not prove independence; the working criterion is
  whether the check could expose a named error the original process could
  have made.
- **Framing error.** The confirmed card frames the wrong problem, and the
  protocol then amplifies the wrong task with full rigor. FRAME lowers the
  frequency; it cannot zero it, because confirmation is the operator's act.
- **Safe commitments.** Expectations too broad to miss, or percentages
  logged where nothing supports calibration. The log fills; nothing is
  learned.
- **Scaffold dependence.** Performance improves inside STRONGBACK and
  disappears in a bare session. Legitimate when known and logged; corrosive
  when attributed to the operator. The bare run in
  [`evals/weekly-transfer.md`](../evals/weekly-transfer.md) exists for this
  mode.
- **Lack of transfer.** Gains hold only in familiar domains or with familiar
  vocabulary. The cold-domain run tests it — read with §5's caveat.
- **Higher-order interactions.** Varying one constraint at a time — even in
  clean pairwise passes — can miss structure that appears only when several
  constraints move together. Two properties make this the quietest mode in
  the registry: the operator gets no advance signal of which class a task
  belongs to, and the miss does not shrink with practice, because it is
  invisible to exactly the procedure being practiced. Partial defense: in
  domains with dense, coupled constraints, vary triples deliberately; when a
  joint pass reveals what pairwise passes missed, label the result
  *structurally approximate* and lower confidence for that class of task,
  not just that task.
- **Excessive process cost.** The loop costs more than the decision is
  worth. The activation rule (`deep` vs `bare`) is the control; when in
  doubt, the question is one line.
- **Instruction fragility.** Some hosts do not reliably hold standing
  instructions. Enforcement there is behavioral; the degradation rule
  applies — the operator runs the gate by hand.
- **Operator dependence.** The protocol cannot outrun a dishonest operator:
  frames confirmed carelessly, artifacts skimmed, closes forced. Every gate
  assumes the operator wants the result checked more than confirmed.
- **Bureaucracy.** The loop turns into paperwork that protects the feeling
  of rigor rather than the quality of the result — compliance theater's cost
  signature. The fix is scope discipline, not more process.

## 4. Who gets what

The hypothesis in §1 does not predict uniform gains, and pretending it does
would be the fastest way to discredit it. Two operator variables should
dominate the outcome:

- **Relational abstraction** — shown two surface-different presentations of
  the same structure, side by side, can you see they are the same? Detection
  with both in front of you: a lower bar than spontaneous transfer, but a
  real one. RUN and the transfer tests lean on it directly.
- **Epistemic orientation** — does closing a question feel like relief or
  like a deadline? Accuracy-seekers hold questions open to find out;
  closure-seekers hold them open to have held them open.

| Abstraction | Orientation | Predicted outcome |
|---|---|---|
| above threshold | accuracy | Real class change: the bottleneck was checking capacity, and checking externalizes. |
| above threshold | closure | Scaffolded gains that vanish in the bare run — which exists for exactly this case. |
| below threshold | accuracy | A sharper existing class: better calibration, fewer unforced errors, no class jump. Worth having; worth naming precisely. |
| below threshold | closure | Articulate surrogates — fluent records of gates that changed nothing. The protocol does not serve this segment, and the sense of rigor it produces can block slower practice that would have helped. |

The threshold is not fixed. It should fall as check density rises, because
more legible independent checks demand less internal discrimination per
check. Whether it falls indefinitely or hits a floor is an open question
(§6). This table is a prediction structure, not a measured result — it says
which public logs should show what, which is what makes it testable.

## 5. Two boundaries worth owning

**Collapse is invisible from inside.** CLOSE's failure has a property the
other failures lack: the faculty that would notice it is the faculty that
failed. An operator whose closing judgment has collapsed — in either
direction — reports "I'm being careful, I'm still open," and that report is
produced by the collapsed process itself. Introspection cannot cross this;
structure can. The weekly bare run is the one observation that does not
route through the possibly-broken instrument, which is why it is part of the
protocol and not an optional extra.

**Cold domains bind the checks too.** In a domain you don't know, you also
don't know what a good check looks like — the domain's failure modes are
exactly what you lack. So the gates are weakest precisely where the load on
them is highest, and the two terms of §1's product are not independent:
check quality is itself domain-bound. A cold-domain result is only as good
as the operator's ability to recognize a bad check. This is why the
cold-domain test scores substance — did the named bottleneck survive
attack — rather than whether the ritual ran, and why a cold pass counts as
weaker evidence than a warm one.

## 6. Evidence and open questions

The public prediction log starts empty. The repo does not yet show that
STRONGBACK improves decisions; it defines how that evidence should be produced.

Open questions:

- Which gates reduce errors on real tasks?
- How much fluent wrongness leaks through legible artifacts (§1)?
- On which task types does process cost exceed benefit?
- What transfers outside the file, and what remains scaffold-dependent?
- Which forms of check catch real misses — and does the abstraction
  threshold (§4) fall with check density, or hit a floor?
- Can higher-order testing (§3) be made cheap enough to run by default?
- How long do operators keep using the loop after novelty fades?
- Does performance improve in the person, the system, or only the pairing?
- Which metrics separate interest in the repo from actual protocol use?

Evidence for transfer is stronger when the gain survives:

1. **Surface mutation:** the same analysis works after renaming and
   re-skinning the problem.
2. **Vocabulary change:** the result does not depend on favorite terms.
3. **Specified deltas:** the operator can name what changed in their
   model-of-me.
4. **Bounded rules:** exceptions do not grow with every anomaly.
5. **Cold-domain test:** the loop produces structure in a domain the
   operator has not worked in recently — read with §5's caveat.
6. **Bare test:** some behavior survives when `STRONGBACK.md` is absent, or the
   operator logs the gain as system-dependent.

These are indicators, not a verdict. Public logs across forks would answer
the open questions faster than stars or visits, which measure interest, not
use.
