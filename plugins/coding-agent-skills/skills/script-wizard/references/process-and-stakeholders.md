# Standards — process improvement, project scoping, multi-stakeholder work

## Contents
- Scoping a project
- Decomposition into phases
- Stakeholder mechanics
- Process improvement specifics
- Decision hygiene

## Scoping a project
- Write the objective as an outcome with a checkable success criterion and a date-shaped
  horizon; a scope without a "we'll know it worked when…" is a wish.
- Name what is explicitly OUT of scope — the cheapest moment to shrink a project is before
  it starts.
- Identify the constraint that binds first (people, data access, approvals, a system
  cutover date) and design the plan around it, not around the work you'd enjoy most.

## Decomposition into phases
- Phases end at decision points or verifiable states, not at effort boundaries — "Phase 1
  complete = the parser passes on all three banks' files" beats "Phase 1 = two weeks."
- Order by dependency and by risk: pull the riskiest unknown as early as possible so its
  failure is cheap (this is the project-shaped version of Diagnose).
- Every phase names an owner, its inputs, its deliverable, and what unblocks the next one.
- Each phase independently useful where possible — a plan that only pays off at the end is
  fragile to any interruption.

## Stakeholder mechanics
- Map who runs it / who consumes it / who approves it / who can veto it — four different
  people with four different questions; answer each in their own terms.
- Distinguish the requester from the beneficiary; when they differ, unstated requirements
  live with the beneficiary.
- Surface disagreement between stakeholders as a named decision for them, not a silent
  compromise by you.

## Process improvement specifics
- Observe the current state before designing the future one; the documented process and
  the actual process are rarely the same thing (go where the work happens).
- Fix root causes but stabilize symptoms first — containment, then countermeasure. Deep
  method here: `continuous-improvement-skills:root-cause-analysis` and
  `continuous-improvement-skills:value-stream-mapping`.
- Every improvement lands on a standard (who does what, when, how verified) or it decays —
  see `continuous-improvement-skills:standard-work`.

## Decision hygiene
- For each real decision: name the options considered, the one recommended, the tradeoff
  accepted, and what evidence would change the call (ADR-shaped, even informally).
- Reversible decisions get made fast with a flagged default; irreversible ones get put to
  the owner with a recommendation.
- Record decisions where the next person will look — a decision that lives only in chat
  will be relitigated.
