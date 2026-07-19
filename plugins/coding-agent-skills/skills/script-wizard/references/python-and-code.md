# Standards — Python, scripts, tools, automation, AI systems

## Contents
- Structure
- Data handling
- Errors & logging
- Determinism & idempotency
- Verification
- When to escalate to the Python persona

## Structure
- Imports at top; logic in small named functions; one guarded entry point
  (`if __name__ == "__main__":`) taking parameters via `argparse` — never hard-coded paths.
- `pathlib.Path` for all paths; constants named at the top, each with a reason.
- One module until size forces more; split by responsibility, not by file-length vanity.

## Data handling
- Validate inputs early: file exists, expected columns present, row count sane — fail loud
  with a message naming the file, the expectation, and what was found instead.
- Preserve identifier fidelity: reference numbers, account tokens, and merchant IDs are
  **strings** — never let a tool float-coerce `0006789599` into `6789599.0` (this rule is
  engine-enforced in the reconciliation projects; see MEMORY).
- Money is integer cents or `Decimal` — never binary floats.
- State the expected encoding and delimiter; don't guess silently.

## Errors & logging
- Catch the *specific* exception you can handle; let everything else raise with context.
  Never `except: pass` — a swallowed error becomes a wrong number.
- `logging` over `print` for anything scheduled or shared: timestamps + levels give you a
  trail when the 2 a.m. run fails.
- Error messages name the thing that failed and the action to take, not just "failed".

## Determinism & idempotency
- Same inputs → same outputs: no time-of-day behavior, no unseeded randomness in anything
  that feeds a report.
- Safe reruns: design so running twice doesn't double-post, double-append, or clobber —
  write to temp then rename, or make outputs keyed and overwritten whole.

## Verification (before presenting)
- Run it. On real-shaped data, not just the happy-path fixture.
- Check a known total against an independent source; check row counts in vs out.
- Rerun and confirm identical output.
- State exactly what was exercised: "tested on X; not tested on Y."

## When to escalate to the Python persona
This reference covers analyst-grade and utility scripts. For production services, libraries,
or anything with users beyond the author — full typing, packaging, CI, property-based tests —
compose with `full-stack-dev-skills:elite-python-engineer`: this skill keeps the workflow
(Frame → … → Audit), that skill supplies the production toolchain and standards.
