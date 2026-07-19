# Standards — documentation, markdown, prose, specifications

## Contents
- Architecture of a document
- Sentences & terms
- Specifications & contract-adjacent language
- Formatting mechanics

## Architecture of a document
- Outline first (Phase 3): every section has a stated purpose; a section whose purpose you
  can't state gets cut before it gets written.
- Lead with the conclusion — the reader who stops after one paragraph should leave with the
  answer. Background follows the answer, never precedes it.
- One idea per section; parallel sections in parallel shape (same heading grammar, same
  depth) so structure carries meaning.
- Write for the named reader from Phase 1. An exec summary and a runbook differ in what
  they omit, not just in length.

## Sentences & terms
- One term per concept, chosen once, used throughout — synonym variety is a defect in
  technical prose because readers assume a new word means a new thing.
- Prefer verbs to nominalizations ("reconcile the account", not "perform reconciliation of
  the account"); prefer the specific to the abstract ("the BSL export", not "the data").
- Every pronoun has an unambiguous antecedent; every "this" is followed by a noun.
- Numbers get units, dates get formats, examples get realistic (sanitized) values.

## Specifications & contract-adjacent language
- Requirements are testable statements: someone must be able to say pass/fail. "Fast" is
  not a requirement; "completes within 5 minutes on 250k rows" is.
- Separate MUST from SHOULD from MAY explicitly, and define any term a lawyer or auditor
  could read two ways.
- Enumerate what is out of scope — silence reads as inclusion.
- Version the document and record what changed; a spec whose history is invisible cannot be
  trusted at audit.

## Formatting mechanics
- Tables for enumerable facts; prose for reasoning — never a table cell holding a paragraph.
- Code, commands, filenames, and literal values in backticks; keep them copy-pasteable.
- Headings state content, not categories ("Purge staged inputs after every run", not
  "Miscellaneous").
- Cut throat-clearing openers ("It is important to note that…") — start with the point.
