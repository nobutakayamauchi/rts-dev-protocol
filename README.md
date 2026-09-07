# rts-dev-protocol

RTS Development Kernel: the vendor-neutral development foundation for RTS, RTS-AGE, ecosystem components, and derived software.

Status: DEVELOPMENT KERNEL / IMPLEMENTATION DRAFT / HUMAN-GATED

## Position

The RTS ecosystem has two independent foundational cores:

- **RTS Trust Core** — decisions, authority, evidence, transitions, checkpoints, and reconstruction.
- **RTS Development Kernel** — development constitution, work/state/test/evidence contracts, adapters, model migration, and repository protection classes.

This repository is the home of the Development Kernel.

It is not RTS core.  
It is not RTS-AGE.  
It is not a runtime implementation or product repository.

RTS-AGE may later execute approved Kernel contracts. AI models, coding agents, tools, and execution engines remain replaceable through adapters.

## Architecture

```text
Human purpose / approval
          |
RTS Development Kernel
          |
 AI / Tool / Repository adapters
          |
        RTS-AGE
          |
    Human authority gate
          |
RTS / components / products
```

RTS may be developed under the Kernel, but RTS must remain independently operable and reconstructable without this repository, RTS-AGE, a provider, an adapter, or an HTML view.

## Core entry points

- Architecture: `docs/architecture/RTS_DEVELOPMENT_KERNEL_V1.md`
- Core Constitution: `docs/contracts/DEVELOPMENT_KERNEL_CORE_CONSTITUTION_V1.md`
- Adapter Contract: `docs/contracts/ADAPTER_CONTRACT_V1.yaml`
- Human Authority: `docs/contracts/HUMAN_AUTHORITY_CONTRACT_V1.md`
- Repository Classes: `docs/policies/REPOSITORY_CLASS_POLICY_V1.yaml`
- Model Migration: `docs/policies/MODEL_MIGRATION_POLICY_V1.yaml`
- RTS TRUST_CORE Adapter Draft: `docs/contracts/RTS_TRUST_CORE_ADAPTER_DRAFT_V1.md`
- Protocol Inventory: `docs/inventory/dev_protocol_inventory.md`

## Stable responsibilities

Use this repository for:

- invariant development rules;
- bounded work and state contracts;
- test and evidence requirements;
- AI/tool/repository adapter contracts;
- model and software replacement procedures;
- repository classification and protection rules;
- human approval boundaries;
- rollback-cheap and reconstructable development procedures;
- non-authoritative, read-only presentation views.

Do not use this repository for:

- RTS canonical records or signed history;
- product or runtime implementation code;
- live deployment orchestration;
- secrets, credentials, or customer data;
- automatic merge, publication, payment, outreach, or authority expansion;
- manufacturing RTS approval, FREEZER state, assessment, or preflight.

## Fundamental rule

```text
SELF_DEVELOPMENT_ALLOWED
SELF_TEST_ALLOWED
SELF_EVIDENCE_PREPARATION_ALLOWED
SELF_APPROVAL_PROHIBITED
SELF_MERGE_PROHIBITED
SELF_AUTHORITY_EXPANSION_PROHIBITED
```

## Current stage

The design direction is approved for implementation. The contract set is being completed in a Draft PR.

Next safe stage:

```text
complete Kernel contract review
→ pilot one thin adapter in a non-core sandbox
→ force interruption and reconstruct from STATE
→ test an alternate AI/tool adapter
→ review evidence
→ expand one repository class at a time
```

RTS remains unchanged and its `TRUST_CORE` adapter stays blocked until RTS prerequisites and a separate human gate are satisfied.
