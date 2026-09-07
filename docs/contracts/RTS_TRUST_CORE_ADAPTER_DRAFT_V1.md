# RTS TRUST_CORE Repository Adapter — Draft v1

Status: BLOCKED / PROPOSAL ONLY / NO BUILD AUTHORITY  
Repository class: `TRUST_CORE`  
Target repository: `nobutakayamauchi/RTS`  
Current action in RTS: NONE

## 1. Position

RTS is one of the systems developed under the RTS Development Kernel, but it is not an ordinary rollout target and does not adopt the Kernel as a runtime dependency.

The connection is a thin development-time repository adapter:

```text
Development Kernel
→ bounded RTS proposal preparation
→ read-only/fail-closed verification
→ RTS governance and human decision
→ possible RTS merge
```

Kernel approval never equals RTS approval.

## 2. RTS responsibility

RTS remains the trust and reconstruction core owning:

- canonical reconstructability rules;
- evidence and integrity semantics;
- authority and approval records;
- state transition history;
- checkpoints and resume semantics;
- append-only or signed history;
- canonical RTS schema and governance decisions.

RTS must remain usable when the Kernel repository, RTS-AGE, AI providers, adapters, tools, and HTML views are unavailable.

## 3. Development Kernel responsibility

The Kernel may provide:

- a bounded work contract;
- fixed read/write/prohibited sets;
- test and evidence requirements;
- adapter compatibility results;
- AI usage limits;
- rollback and interruption-recovery rules;
- a proposed evidence packet for human and RTS review.

The Kernel must not create RTS authority, canonicalize its own output, or change RTS governance.

## 4. Current prerequisite block

Current RTS Shape Up order records:

```text
Stage 1  Measure and map                                  COMPLETE
Stage 2  Classify canonical/generated/history/fixture     NEXT
Stage 3  Unify operator and AI entry points               LATER
```

The adapter concerns Stage 3-style development entry behavior. It remains blocked until Stage 2 classification/reference analysis is complete and a human authorizes an isolated RTS proposal.

## 5. Proposed local adapter shape

Illustrative only; exact RTS paths require Stage 2 findings.

```yaml
kernel:
  version: "1.0"
  commit: "<fixed-kernel-commit>"
repository:
  name: "nobutakayamauchi/RTS"
  class: "TRUST_CORE"
  base_commit: "<fixed-rts-base-commit>"
permissions:
  allowed:
    - inspect
    - classify
    - propose
    - validate
    - test_on_isolated_branch
  prohibited:
    - direct_default_branch_write
    - canonical_write_from_adapter
    - self_approval
    - signed_history_rewrite
    - freezer_approval_manufacture
    - authority_expansion
required_evidence:
  - exact_diff
  - deterministic_test_results
  - signed_history_byte_invariance
  - checkpoint_byte_invariance
  - rollback_point
  - uncertainty_report
  - separate_human_approval
```

## 6. Required preconditions

All must be true before an RTS proposal PR is opened:

- [ ] RTS Stage 2 path classification is merged.
- [ ] Candidate documentation/schema/test locations are reference-mapped.
- [ ] No existing canonical rule already owns the proposed meaning.
- [ ] Proposal classification is explicitly non-canonical until RTS decides otherwise.
- [ ] Fixed RTS base commit is recorded.
- [ ] Rollback is one bounded revert or equivalent reviewed path.
- [ ] Signed history, checkpoints, fingerprints, and chains are protected.
- [ ] No runtime, authority, deployment, or external behavior change is implied.
- [ ] A human separately authorizes opening the RTS proposal PR.

## 7. Two-stage human gate

### Gate A — proposal authorization

Authorizes only an isolated RTS proposal branch and read-only/fail-closed tests.

### Gate B — merge/canonical decision

Occurs only after diff, tests, invariance, uncertainty, and rollback are reviewed under RTS governance.

Passing Gate A or automated tests does not pass Gate B.

## 8. Required acceptance tests

A future adapter proposal must prove:

1. RTS reconstruction does not depend on a model, provider, Kernel, RTS-AGE, adapter, or HTML view.
2. Changing an AI/tool adapter does not change RTS authority.
3. Missing or mismatched Kernel/adapter versions fail closed.
4. Required input and evidence hashes are checked.
5. Signed history, checkpoints, and protected records remain byte-for-byte unchanged unless a separately authorized task explicitly targets them.
6. No runtime, deployment, publication, payment, customer, or external action is introduced.
7. No automatic FREEZER, assessment, preflight, approval, or canonical record is manufactured.
8. The entire proposal can be rolled back through one bounded reviewed operation.

## 9. Permanent prohibitions

- Do not copy the entire Development Kernel into RTS.
- Do not make `rts-dev-protocol` a runtime dependency.
- Do not make RTS-AGE or an AI provider necessary for reconstruction.
- Do not add automatic cross-repository synchronization.
- Do not add provider-specific canonical fields.
- Do not make HTML canonical.
- Do not rewrite signed history to reference the Kernel.
- Do not allow the adapter to approve, merge, deploy, or expand authority.

## 10. Current state

```text
RTS_CLASSIFIED_AS_TRUST_CORE
DEVELOPMENT_TIME_ADAPTER_MODEL_SELECTED
RTS_RUNTIME_INDEPENDENCE_REQUIRED
NO_RTS_FILE_CHANGED
NO_RTS_AUTHORITY_CHANGED
RTS_STAGE_ORDER_PRESERVED
TRUST_CORE_ADAPTER_BLOCKED_PENDING_STAGE_2_AND_HUMAN_GATE_A
```