# AI-Efficient Development Protocol v1

Status: DRAFT / HUMAN REVIEW REQUIRED  
Authority: development procedure only  
Canonical RTS adoption: NOT AUTHORIZED

## 1. Purpose

Produce better development outcomes with the minimum necessary AI context, calls, retries, and duplicated documentation while preserving safety, evidence, rollbackability, and reconstruction.

This protocol does not make an AI authoritative. AI remains a replaceable worker operating inside human-approved scope.

## 2. Four-layer structure

### Layer 1 — invariant development principles

These rules do not change when the model, provider, tool, language, or repository changes.

1. State the purpose as an input → processing → output transformation.
2. Keep the canonical specification outside chat.
3. Separate confirmed facts, assumptions, hypotheses, and unknowns.
4. Define the minimum success condition before implementation.
5. Define out-of-scope work and prohibited actions.
6. Keep WIP at one bounded slice unless explicitly approved.
7. Define rollback before material change.
8. Bind completion claims to evidence.
9. Separate automated tests from human device/operational verification.
10. Do not call unexecuted work complete or verified.
11. Preserve a deterministic restart point.
12. Keep merge, deployment, publication, payment, outreach, and authority changes behind human gates.

### Layer 2 — AI adaptation profile

Only AI-specific operating conditions belong here:

- tools and repository access;
- shell/test/browser capability;
- context and file-loading strategy;
- output format;
- retry and usage budget;
- known behavioral risks;
- unsupported actions;
- required human handoffs.

Changing AI must not silently change project purpose, success criteria, authority, or evidence standards.

### Layer 3 — project specification

Each project defines only its own:

- purpose;
- inputs and outputs;
- minimum success condition;
- acceptance tests;
- allowed files and prohibited areas;
- data/safety boundaries;
- rollback point;
- human decisions.

### Layer 4 — execution state and evidence

Current position is recorded as compact structured data:

- specification and AI-profile versions;
- current phase;
- completed and failed test IDs;
- evidence references;
- unknowns;
- next bounded action;
- rollback commit;
- required human gate.

Long chat history is not a canonical state source.

## 3. Minimal operating loop

```text
INTAKE
→ SCOPE LOCK
→ AI PROFILE SELECT
→ IMPLEMENT ONE SLICE
→ RUN DETERMINISTIC TESTS
→ HUMAN VERIFY WHEN REQUIRED
→ RECORD EVIDENCE
→ HUMAN MERGE / STOP
```

A normal low-risk slice should target three AI work cycles:

1. compile the bounded specification;
2. implement and run automated tests;
3. audit differences and prepare handoff.

Default maximum: five cycles. After two repeated failures without new evidence, stop retrying and reduce scope or escalate to human review.

## 4. Context minimization

Every task must declare a read set and a write set.

```yaml
read:
  - PROJECT.yaml
  - STATE.yaml
  - relevant source file
  - relevant test file
write:
  - relevant source file
  - relevant test file
  - STATE.yaml
forbidden:
  - unrelated repositories
  - historical chat logs
  - signed history
  - secrets
```

Load one to three relevant skills only. Read original logs only when the compact state lacks enough evidence.

## 5. Evidence standard

Each material claim must resolve to one of:

- `VERIFIED_AUTOMATED` — deterministic test or static check;
- `VERIFIED_HUMAN` — recorded human observation;
- `HUMAN_ATTESTED` — human report without connector/tool verification;
- `INFERRED` — reasoned conclusion with cited basis;
- `UNVERIFIED` — not yet checked;
- `WITHHELD` — intentionally not claimed.

Code creation alone is not evidence that behavior works.

## 6. AI usage budget

```yaml
normal_cycles: 3
maximum_cycles: 5
maximum_repeat_without_new_evidence: 2
maximum_loaded_skills: 3
maximum_active_slice_count: 1
spec_changes_after_lock: 0
production_auto_deploy: false
automatic_merge: false
```

Budget exhaustion does not authorize lower safety. Reduce scope in this order:

1. optional explanation and decoration;
2. secondary output formats;
3. convenience features;
4. secondary input formats;
5. nonessential integrations;
6. stop at the minimum success condition.

## 7. Model-change procedure

A new or materially changed AI must pass compatibility checks before taking the primary implementation role.

Required checks:

1. obey allowed/forbidden file scope;
2. preserve the locked specification;
3. fix only the failing surface;
4. distinguish unknown from confirmed;
5. update structured state correctly;
6. avoid secret disclosure;
7. preserve rollback information;
8. stop at a human authority gate.

Disposition:

- `GREEN`: same role permitted;
- `YELLOW`: restricted role or extra guardrails;
- `RED`: not permitted on the main development path.

## 8. Repository rollout

Rollout is never ecosystem-wide in one operation.

```text
central draft
→ human review
→ non-core pilot
→ forced interruption/reconstruction test
→ evidence review
→ one repository-class adapter
→ separate approval for RTS integration
→ gradual opt-in rollout
```

Each repository receives only a thin adapter. The central protocol remains the reusable procedure source; repository-specific code and authority remain local.

## 9. HTML rule

HTML is a human-readable presentation layer, not the canonical authority source.

HTML must be:

- self-contained;
- free of external scripts, fonts, trackers, and network calls;
- readable on approximately 320px mobile width;
- explicit about source version and derived/non-authoritative status;
- incapable of merge, deployment, outreach, payment, or secret handling.

Structured YAML/JSON and reviewed Markdown remain the machine/review sources until RTS separately adopts a canonical schema.

## 10. Human gates

Human approval is mandatory before:

- changing project purpose or minimum success;
- modifying canonical RTS rules or records;
- merging to a protected/default branch;
- production deployment;
- publication or external communication;
- payment, contract, or customer action;
- handling real confidential data;
- changing authority boundaries;
- expanding rollout to another repository class.

## 11. Completion definition

A slice is complete only when:

1. the minimum success condition is met;
2. required automated tests pass;
3. required human verification is recorded;
4. evidence and unknowns are separated;
5. rollback is available;
6. the next action or stop decision is explicit;
7. no prohibited authority was exercised.

## 12. Non-goals

This protocol does not authorize:

- automatic RTS adoption;
- replacement of existing canonical schemas;
- rewriting signed history;
- automatic FREEZER creation or approval;
- automatic multi-repository modification;
- deployment automation;
- external actions;
- secrets or real customer-data ingestion;
- removal of existing project documentation before migration evidence exists.
