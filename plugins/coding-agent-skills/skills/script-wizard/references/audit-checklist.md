# Audit checklist (Phase 5 — run adversarially, after building)

Switch mindsets first: you are no longer the builder defending the work; you are the
skeptical expert paid to find why it fails. Every "obviously fine" deserves one look.

## Contents
- Correctness
- Robustness
- Readability & misreading
- Dependencies & environment
- Fitness to the frame
- Calibration of claims

## Correctness
- [ ] Does each requirement from Phase 1 have a place in the artifact where it is satisfied?
- [ ] Trace one real input end-to-end by hand — does the output match what you claimed?
- [ ] Any numbers: do totals tie? Do signs, units, and rounding behave at the boundaries?
- [ ] Off-by-one sweep: first row, last row, boundaries of every range and window.

## Robustness (what breaks)
- [ ] Empty input; single row; duplicate rows; nulls in every optional field.
- [ ] Malformed data: wrong encoding, wrong delimiter, string where a number belongs,
      leading-zero identifiers.
- [ ] Scale: 10× the expected volume — what degrades first?
- [ ] Every external dependency: what does the artifact do when it is down, slow, or wrong?
- [ ] Partial failure: if it dies halfway, what state is left behind, and is a rerun safe?

## Readability & misreading
- [ ] What could a reasonable reader misread? Ambiguous names, overloaded terms,
      instructions that admit two interpretations.
- [ ] Is every non-obvious choice's *why* recorded where the reader will meet it?
- [ ] Parallel things presented in parallel form; one term per concept throughout.

## Dependencies & environment
- [ ] Which dependency is most fragile, and does the artifact say so?
- [ ] Versions/permissions/paths assumed but not stated?
- [ ] Will it run on the user's machine, not just here? What must they install or configure?

## Fitness to the frame
- [ ] Does this answer the Phase 1 objective, or a nearby easier question?
- [ ] Would each stakeholder named in Phase 1 accept this? Who pushes back, and on what?
- [ ] Is anything present that isn't earning its place? Cut it.

## Calibration of claims
- [ ] Everything labeled "tested" was actually executed; everything else is labeled
      inferred, assumed, or untested.
- [ ] No invented sources, citations, or results.
- [ ] The riskiest remaining unknown is named in the Risks section, not hidden.

**Exit rule:** the audit is done when it has found something (fix it) or when you can say
specifically why each category above came up clean — "no findings" without the pass is not
an audit.
