# RTS Development Kernel — Core Constitution v1

Status: DESIGN DIRECTION APPROVED / IMPLEMENTATION DRAFT  
Authority: development procedure only  
Automatic ecosystem adoption: NOT AUTHORIZED

## 1. Purpose

Provide a stable development foundation for RTS, RTS-AGE, ecosystem components, and derived software while minimizing unnecessary AI calls, context, retries, and vendor dependence.

The Kernel defines how development is prepared, bounded, tested, evidenced, paused, resumed, and handed to human authority. It does not make an AI, tool, engine, repository, or the Kernel itself authoritative.

## 2. Relationship to RTS

The ecosystem has two independent foundations:

- `RTS`: trust, authority, evidence, state transition, checkpoint, and reconstruction core.
- `RTS Development Kernel`: development constitution, work/state/test/evidence contracts, adapter rules, model migration, and repository protection classes.

RTS may be developed under the Kernel. RTS must remain independently operable and reconstructable without the Kernel, RTS-AGE, a provider, an adapter, or an HTML renderer.

## 3. Invariant development principles

These rules do not change when the model, provider, tool, language, execution engine, or repository changes.

1. State purpose as input → processing → output.
2. Keep the locked specification outside chat.
3. Separate confirmed facts, assumptions, hypotheses, unknowns, and withheld claims.
4. Define minimum success before implementation.
5. Define non-goals, prohibited actions, read set, and write set.
6. Keep WIP at one bounded slice unless a human approves otherwise.
7. Define rollback before material change.
8. Bind completion claims to evidence IDs.
9. Separate automated tests, human operational tests, and human attestation.
10. Never call unexecuted or unreproduced work verified.
11. Preserve a deterministic restart point.
12. Keep merge, deployment, publication, payment, outreach, protected-data use, and authority changes behind human gates.
13. Replace software through versioned adapters rather than rewriting the project contract.
14. Permit self-development but prohibit self-approval, self-merge, and self-authority expansion.

## 4. Contract layers

### Layer 1 — Core Constitution

Defines invariant principles, authority limits, evidence meanings, stopping rules, and completion rules.

### Layer 2 — Adapter and Profile Layer

Contains only replaceable implementation conditions:

- model/provider or coding agent;
- tools and repository access;
- execution engine;
- context-loading strategy;
- capabilities and unavailable operations;
- usage/retry budget;
- compatibility disposition;
- required human handoffs.

Changing an adapter must not silently change project purpose, minimum success, evidence standards, repository class, or authority.

### Layer 3 — Project Contract

Each project defines only its own:

- purpose;
- inputs and outputs;
- minimum success;
- acceptance tests;
- allowed and prohibited surfaces;
- data and safety boundaries;
- rollback point;
- required human decisions.

### Layer 4 — State, Tests, and Evidence

Current position is compact structured data containing:

- Kernel, project, adapter, and test versions;
- current phase and active slice;
- completed, failed, and blocked test IDs;
- evidence references and hashes;
- unknowns and withheld claims;
- next bounded action;
- rollback commit or recovery reference;
- pending human gate.

Long chat history is never the canonical state source.

## 5. Minimal operating loop

```text
INTAKE
→ CLASSIFY REPOSITORY
→ LOCK PURPOSE / SCOPE / TESTS
→ PIN KERNEL AND ADAPTERS
→ IMPLEMENT ONE SLICE
→ RUN DETERMINISTIC TESTS
→ HUMAN VERIFY WHEN REQUIRED
→ RECORD EVIDENCE / UNKNOWN
→ HUMAN APPROVE, MERGE, DEFER, OR STOP
```

A normal low-risk slice targets three AI work cycles:

1. compile the bounded work packet;
2. implement and run automated tests;
3. audit differences and prepare evidence/handoff.

Default maximum: five cycles. After two repeated failures without new evidence, stop retrying and reduce scope, change adapter, or escalate to human review.

## 6. Context minimization

Every task declares a read set and a write set.

```yaml
read:
  - PROJECT.yaml
  - STATE.yaml
  - TESTS.yaml
  - selected adapter/profile
  - relevant source and test files
write:
  - bounded source/test files
  - STATE.yaml
  - evidence packet
forbidden:
  - unrelated repositories
  - unbounded historical chat
  - signed history
  - secrets unless separately authorized
```

Load one to three relevant skills or instruction modules only. Read original logs only when compact state lacks enough evidence.

## 7. Evidence classification

Each material claim resolves to one of:

- `VERIFIED_AUTOMATED`: deterministic test or static check.
- `VERIFIED_HUMAN`: recorded direct human observation.
- `HUMAN_ATTESTED`: human report without connector/tool verification.
- `INFERRED`: reasoned conclusion with identified basis.
- `UNVERIFIED`: not checked.
- `WITHHELD`: intentionally not claimed.

Code creation, AI confidence, or a successful commit is not evidence that behavior works.

## 8. AI and execution budget

```yaml
normal_cycles: 3
maximum_cycles: 5
maximum_repeat_without_new_evidence: 2
maximum_loaded_skills: 3
maximum_active_slice_count: 1
spec_changes_after_lock: 0
automatic_merge: false
production_auto_deploy: false
```

Budget exhaustion never lowers safety. Reduce scope in this order:

1. decorative explanation;
2. secondary output formats;
3. convenience features;
4. secondary input formats;
5. nonessential integrations;
6. stop at minimum success.

## 9. Adapter replacement procedure

A new or materially changed AI, tool, repository connector, or execution engine must pass compatibility tests before taking its role.

Required checks:

1. obey allowed and prohibited scope;
2. preserve locked specification and tests;
3. modify only the failing/bounded surface;
4. distinguish unknown from confirmed;
5. update structured state correctly;
6. avoid secret disclosure;
7. preserve rollback and input hashes;
8. stop at human authority gates;
9. produce the stable execution/evidence output contract.

Disposition:

- `GREEN`: same role permitted.
- `YELLOW`: restricted role or additional guardrails.
- `RED`: prohibited on the requested development path.
- `UNTESTED`: fail closed for material work.

## 10. Repository protection

Every repository is assigned a class under `REPOSITORY_CLASS_POLICY_V1.yaml`.

RTS is `TRUST_CORE` and receives the maximum protection level:

- isolated proposal branch only;
- fixed base commit;
- read-only/fail-closed testing first;
- byte-invariance checks for signed history and checkpoints;
- separate implementation-direction and merge gates;
- no automatic canonical write, merge, deployment, or self-approval.

## 11. Self-development rule

The Kernel may be used to develop itself, RTS-AGE, adapters, RTS proposals, components, and products.

```text
SELF_DEVELOPMENT_ALLOWED
SELF_TEST_ALLOWED
SELF_EVIDENCE_PREPARATION_ALLOWED
SELF_APPROVAL_PROHIBITED
SELF_MERGE_PROHIBITED
SELF_AUTHORITY_EXPANSION_PROHIBITED
```

A material Kernel change requires a versioned contract change and a human approval record.

## 12. HTML and derived views

HTML is a human-readable presentation layer, never a canonical authority source.

HTML must be:

- self-contained;
- free of external scripts, fonts, trackers, and network calls;
- readable at approximately 320px width;
- explicit about source version and derived/non-authoritative status;
- incapable of merge, deployment, outreach, payment, secret handling, or authority change.

## 13. Completion definition

A slice is complete only when:

1. minimum success is met;
2. required automated tests pass;
3. required human verification is recorded;
4. evidence, inference, unknowns, and withheld claims are separated;
5. rollback is available;
6. the next action or stop decision is explicit;
7. no prohibited authority was exercised;
8. output follows the stable adapter contract.

## 14. Non-goals

This Constitution does not authorize:

- automatic RTS adoption or canonical write;
- replacing existing RTS governance or schemas;
- rewriting signed or append-only history;
- automatic FREEZER creation, approval, or preflight manufacture;
- automatic multi-repository mutation;
- automatic merge or production deployment;
- external communication, payment, contract, or customer action;
- secret or real protected-data ingestion without separate approval;
- removal of existing project documentation before migration evidence exists.

## 15. Current decision

```text
DEVELOPMENT_KERNEL_SELECTED_AS_DEVELOPMENT_FOUNDATION
RTS_REMAINS_SEPARATE_TRUST_FOUNDATION
ADAPTER_BASED_REPLACEABILITY_REQUIRED
RTS_AGE_REMAINS_REPLACEABLE_EXECUTION_ENGINE
SELF_DEVELOPMENT_ALLOWED
SELF_APPROVAL_PROHIBITED
GRADUAL_OPT_IN_ROLLOUT_ONLY
RTS_REPOSITORY_UNCHANGED
```