# Contributing

Substantive changes run the protocol. A protocol about verified thinking that
merges unverified claims would be its own counterexample.

## What passes without the loop

Mechanical fixes: typos, dead links, formatting. Open the PR, write
"mechanical," delete the rest of the template. Done.

## What runs the loop

Anything that changes what the protocol says — gate wording, state
templates, ENGINE claims, README framing. For these, the PR template asks
for three things, and the PR is judged on them:

1. **Your logged commitment**, written before the change: what you expect
   it to improve or what failure you expect it to avoid. Copy the row from
   your own `predictions.log`.
2. **One attack on your own change.** Name the plausible error in your
   original process that the check could expose, why the check's mechanism
   differs, and which blind spots remain shared. "I re-read it carefully"
   does not count.
3. **A failure-pattern check:** which mode in
   [`evals/failure-pattern-checklist.md`](evals/failure-pattern-checklist.md)
   — canonical registry in [`docs/ENGINE.md`](docs/ENGINE.md) §3 — your
   change could be an instance of, and why it is not.

## Hard constraints

- **STRONGBACK.md stays under 100 lines.** If your change adds lines there,
  cut at least as many in the same file. A kernel that bloats has broken
  the principle it teaches; that is a rejected PR regardless of content.
- **Plain language.** Dense beats long. No marketing vocabulary, no
  throat-clearing. Qualify claims when accuracy requires it.
- **Claims must be things the files deliver.** Theory goes to ENGINE.md
  and carries its boundaries with it.

## Forks

Forking is the distribution model, not a fallback. Strip it, rewrite it,
rebrand it for your stack — a fork that becomes someone's standard is the
protocol working. Upstream what generalizes; keep what doesn't.
