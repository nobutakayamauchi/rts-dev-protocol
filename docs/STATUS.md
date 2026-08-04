# rts-dev-protocol Status

Status: DEVELOPMENT KERNEL / DESIGN APPROVED / IMPLEMENTATION DRAFT

## Current position

This repository is the home of the RTS Development Kernel, the development foundation used to prepare, constrain, test, evidence, pause, resume, and hand off work across RTS-related repositories.

The design direction was explicitly selected on 2026-08-04. Repository merge, rollout, and connected-repository changes remain separately human-gated.

## Ecosystem boundary

### RTS

RTS is the separate trust and reconstruction foundation. It owns canonical decision, authority, evidence, transition, checkpoint, integrity, and reconstruction rules.

RTS is not changed by the current Kernel Draft PR. RTS must remain independently usable without this repository or any provider/runtime adapter.

### RTS Development Kernel

This repository owns:

- core development constitution;
- work/project/state/test/evidence contracts;
- AI/tool/execution/repository adapter contracts;
- model and software migration policy;
- repository protection classes;
- human authority and stopping rules;
- reviewable templates and derived read-only views.

### RTS-AGE

RTS-AGE is a replaceable execution engine that may later run approved Kernel contracts. It cannot manufacture approval or canonical RTS state.

### Connected repositories

Products, runtimes, governance repositories, components, sandboxes, and RTS itself retain local ownership and receive only thin, version-pinned repository adapters.

## Current implemented Draft set

- Kernel architecture;
- Core Constitution;
- Adapter Contract;
- Human Authority Contract;
- Repository Class Policy;
- Model Migration Policy;
- Project/State/Tests/AI Profile templates;
- RTS TRUST_CORE Adapter Draft;
- protocol inventory;
- derived read-only HTML view.

## Permanent safety rules

- no direct default-branch write for material work;
- no automatic merge or deployment;
- no self-approval or authority expansion;
- no automatic RTS canonical write;
- no signed-history rewrite;
- no automatic multi-repository mutation;
- no secrets or protected data without separate authorization;
- no success claim without evidence;
- no lowering protection because AI budget is exhausted.

## Current decisions

```text
TWO_FOUNDATIONAL_CORES_SELECTED
RTS_IS_TRUST_AND_RECONSTRUCTION_CORE
RTS_DEVELOPMENT_KERNEL_IS_DEVELOPMENT_FOUNDATION
RTS_AGE_IS_REPLACEABLE_EXECUTION_ENGINE
ADAPTER_BASED_REPLACEABILITY_REQUIRED
SELF_DEVELOPMENT_ALLOWED
SELF_APPROVAL_PROHIBITED
RTS_REPOSITORY_UNCHANGED
DRAFT_PR_REVIEW_AND_NON_CORE_PILOT_NEXT
```
