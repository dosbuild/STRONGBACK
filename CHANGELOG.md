# Changelog

Versions are honest: 0.x means the kernel is complete and the edges are
still being measured in public.

## [0.1.0] — 2026-09-04

**Initial kernel release.**

STRONGBACK ships as one file. Add `STRONGBACK.md` to an AI instruction surface
and run the five-gate loop on complex, deferrable work: FRAME, PREDICT, RUN,
ATTACK, CLOSE.

Shipped:

- `STRONGBACK.md` — the kernel: the split, activation rule, five gates,
  prohibitions, scoreboard, scope. Under 100 lines by rule.
- `protocols/` — one page per gate: the problem, the rule, the failure
  pattern, and the test that catches it.
- `state/` — externalized memory, kept by the operator: task card,
  zero-state predictions log, decisions log, prohibitions, model-of-me.
- `evals/` — the weekly transfer test (cold-domain and bare runs) and the
  failure-pattern checklist. The canonical failure registry is ENGINE §3.
- `docs/ENGINE.md` — the working hypothesis with its strongest counter
  named, the failure registry, who the protocol serves and who it does
  not, and the transfer indicators.

Decisions worth naming:

- The install names surfaces, not menu paths: menus date, the paste doesn't.
- The prediction log starts empty. The first row will be committed before
  its outcome is known, and misses will remain visible.
- State files are operator-kept: a model running only in a hosted chat cannot
  see or write the repo, so "log the row" means the operator writes the row.

Not shipped, on purpose: an app, a build, CI, badges, a wiki. v0.1 is a
file protocol.

The Map marks seven nodes beyond the kernel — organs around the loop
(candidates: state hygiene, delegation limits, integrity monitoring), not
additional gates. They are not in this release; future 0.x releases can add
them one file at a time.

Direction for 0.2: choose the first organ by what breaks first in public use.
