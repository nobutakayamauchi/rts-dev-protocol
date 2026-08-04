# RTS Development Kernel Inventory

Status: IMPLEMENTATION DRAFT / REVIEW REQUIRED

This inventory is documentation and contract material only. It changes no RTS authority, runtime, deployment, product behavior, or external action.

## Classification rules

- `DESIGN_APPROVED`: architecture direction selected for implementation; merge and rollout remain separate gates.
- `IMPLEMENTATION_DRAFT`: concrete contract exists but is not yet merged/released.
- `BLOCKED`: must not proceed until named prerequisites and human authorization exist.
- `DERIVED`: non-authoritative presentation generated from reviewed sources.
- `PILOT_REQUIRED`: requires bounded non-core evidence before broader use.

## Kernel inventory

| Item | Path | Status | Purpose | Next smallest safe action |
|---|---|---|---|---|
| Development Kernel architecture | `docs/architecture/RTS_DEVELOPMENT_KERNEL_V1.md` | DESIGN_APPROVED | define two foundations and complete dependency structure | review internal consistency |
| Core Constitution | `docs/contracts/DEVELOPMENT_KERNEL_CORE_CONSTITUTION_V1.md` | IMPLEMENTATION_DRAFT | invariant development, evidence, budget, completion, and stopping rules | validate against all templates |
| Adapter Contract | `docs/contracts/ADAPTER_CONTRACT_V1.yaml` | IMPLEMENTATION_DRAFT / PILOT_REQUIRED | replace AI, tools, engines, and repository connectors without changing project authority | parse and test with one sandbox adapter |
| Human Authority Contract | `docs/contracts/HUMAN_AUTHORITY_CONTRACT_V1.md` | IMPLEMENTATION_DRAFT | prohibit self-approval and identify human-only gates | review approval-record fields |
| Repository Class Policy | `docs/policies/REPOSITORY_CLASS_POLICY_V1.yaml` | IMPLEMENTATION_DRAFT | apply increasing protection from SANDBOX to TRUST_CORE | validate local adapter inheritance |
| Model Migration Policy | `docs/policies/MODEL_MIGRATION_POLICY_V1.yaml` | IMPLEMENTATION_DRAFT / PILOT_REQUIRED | classify replacement AI as GREEN/YELLOW/RED | run compatibility test on alternate adapter |
| RTS TRUST_CORE Adapter | `docs/contracts/RTS_TRUST_CORE_ADAPTER_DRAFT_V1.md` | BLOCKED | connect Kernel to RTS at development time without runtime dependency | wait for RTS Stage 2 and Gate A authorization |
| Project template | `templates/PROJECT.template.yaml` | IMPLEMENTATION_DRAFT / PILOT_REQUIRED | lock purpose, scope, minimum success, and rollback | instantiate in sandbox |
| State template | `templates/STATE.template.yaml` | IMPLEMENTATION_DRAFT / PILOT_REQUIRED | preserve compact restart state and unknowns | force interruption/reconstruction test |
| Tests template | `templates/TESTS.template.yaml` | IMPLEMENTATION_DRAFT / PILOT_REQUIRED | bind completion to automated/human evidence IDs | verify evidence classifications |
| AI profile template | `templates/AI_PROFILE.template.yaml` | IMPLEMENTATION_DRAFT / PILOT_REQUIRED | record model-specific capability and limits | bind to Adapter Contract |
| Repository adapter template | `templates/REPOSITORY_ADAPTER.template.yaml` | IMPLEMENTATION_DRAFT / PILOT_REQUIRED | bind local repository class and authority to a fixed Kernel version | create after contract consistency check |
| Human-readable HTML view | `docs/html/RTS_DEVELOPMENT_KERNEL_V1.html` | DERIVED | mobile-readable, network-free architecture and operating view | review visually; never treat as canonical |

## Foundation boundary

### RTS Trust Core

RTS owns canonical decisions, authority, evidence, transitions, checkpoints, integrity, and reconstruction. It must remain independently usable when the Development Kernel, RTS-AGE, adapters, providers, tools, and HTML views are unavailable.

### RTS Development Kernel

This repository owns development constitution and contracts. It may prepare development and evidence packets but cannot approve or canonicalize its own work.

### RTS-AGE

RTS-AGE is a replaceable execution engine. It may execute approved work contracts and return evidence. It cannot manufacture human or RTS authority.

### Connected repositories

Each repository retains local behavior, code, tests, release decisions, and governance. It receives only a thin version-pinned adapter.

## Permanent dependency rule

```text
Development time: connected repository may use a pinned Kernel contract.
Runtime/reconstruction time: repository remains independent by default.
RTS special case: development-time adapter allowed later; reconstruction-time Kernel dependency prohibited.
```

## Stop conditions

Stop and require human review if work would:

- change RTS authority or canonical record semantics;
- rewrite signed or append-only history;
- bypass FREEZER, preflight, checkpoint, or human approval;
- allow self-approval, self-merge, or self-authority expansion;
- add deployment, external contact, payment, publication, contract, or customer action;
- expose credentials, private data, or protected information;
- lower repository protection automatically;
- apply the Kernel ecosystem-wide without per-repository evidence and rollback;
- make RTS runtime or reconstruction depend on this repository, an adapter, provider, or HTML view.
