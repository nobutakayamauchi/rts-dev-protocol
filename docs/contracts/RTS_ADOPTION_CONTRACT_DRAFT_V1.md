# RTS Adoption Contract — Draft v1

Status: BLOCKED / PROPOSAL ONLY / NO BUILD AUTHORITY  
Target repository: `nobutakayamauchi/RTS`  
Current action in RTS: NONE

## 1. Why RTS requires a separate contract

RTS is the trust and reconstruction core. It defines canonical record formats, append-only history, integrity and evidence rules, checkpoint/resume semantics, and governance boundaries.

The AI-efficient development protocol may eventually depend on RTS rules. It must not invert that dependency or make RTS dependent on a model, provider, runtime, HTML viewer, or development-procedure repository.

## 2. Current block

The current RTS shape-up order records:

```text
Stage 1  Measure and map                         COMPLETE
Stage 2  Classify canonical / generated / history / fixture  NEXT
Stage 3  Unify operator and AI entry points      LATER
```

This proposal concerns Stage 3 behavior and therefore must not be inserted into RTS before Stage 2 classification and reference analysis are completed and reviewed.

## 3. Permanent authority boundary

If later adopted:

### RTS owns

- canonical reconstructability rules;
- evidence classifications and integrity expectations;
- authority and approval boundaries;
- checkpoint and resume semantics;
- append-only or signed history rules;
- canonical schema decisions.

### rts-dev-protocol owns

- reusable development procedures;
- AI implementation contracts;
- context minimization guidance;
- model migration procedure;
- repository rollout checklists;
- non-authoritative HTML presentation guidance.

### RTS-AGE may own later

- loading an approved protocol;
- selecting a bounded AI profile;
- preparing project adapters;
- executing approved tasks;
- returning evidence packets.

RTS-AGE must not manufacture RTS approval, rewrite canonical state, or treat execution output as canonical merely because an AI produced it.

### Product/component repositories own

- product-specific code;
- local project specification;
- local tests and operational behavior;
- local rollback and release decisions.

## 4. Proposed RTS integration surface

The smallest safe future RTS change is documentation and schema review only.

Possible later artifacts, subject to RTS classification results:

```text
docs/proposals/AI_DEVELOPMENT_ADAPTER_CONTRACT_V1.md
schemas/proposals/ai_development_adapter.schema.json
fixtures/proposals/ai_development_adapter/
tests/read_only/test_ai_development_adapter_contract.py
```

These paths are illustrative only. Stage 2 classification must determine whether they are correct and whether similar canonical/proposal locations already exist.

## 5. Required preconditions

All must be true before an RTS implementation PR is opened:

- [ ] Stage 2 path classification is merged.
- [ ] References to candidate schema and documentation locations are mapped.
- [ ] No existing canonical schema already owns the same meaning.
- [ ] The proposal is classified as `PROPOSAL_ONLY` or another approved non-canonical category.
- [ ] The change does not rewrite signed or append-only history.
- [ ] The change does not change runtime or authority.
- [ ] A fixed base commit and rollback plan are recorded.
- [ ] Human approval explicitly authorizes an RTS proposal PR.

## 6. Future acceptance tests

A future read-only RTS proposal must prove:

1. reconstructability does not depend on a specific AI/model/provider;
2. HTML is derived and non-authoritative;
3. changing AI profiles does not change project authority;
4. missing profile, invalid version, or evidence mismatch fails closed;
5. signed history and existing checkpoints remain byte-for-byte unchanged;
6. no runtime, deployment, external action, publication, or customer behavior is added;
7. the proposal can be removed by reverting one bounded commit/PR.

## 7. Prohibited shortcuts

Do not:

- copy the central protocol wholesale into RTS;
- make `rts-dev-protocol` a runtime dependency;
- create automatic cross-repository sync;
- add provider-specific canonical fields;
- make HTML a canonical state source;
- update existing signed records to reference the new protocol;
- auto-create FREEZER records, assessments, or preflights;
- merge before explicit human review.

## 8. Current decision

```text
RTS_REVIEWED_AS_FOUNDATIONAL_CORE
NO_RTS_FILE_CHANGED
NO_RTS_AUTHORITY_CHANGED
RTS_STAGE_ORDER_PRESERVED
ADOPTION_CONTRACT_DRAFTED_OUTSIDE_RTS
WAIT_FOR_STAGE_2_CLASSIFICATION_AND_HUMAN_AUTHORIZATION
```
