# RTS Development Kernel Architecture v1

Status: DESIGN DIRECTION APPROVED / IMPLEMENTATION DRAFT  
Decision date: 2026-08-04  
Authority: development architecture only; repository merge remains human-gated

## 1. Decision

The RTS ecosystem uses two independent foundational cores.

```text
TRUST FOUNDATION                  DEVELOPMENT FOUNDATION
RTS                               RTS Development Kernel
- decisions                       - development constitution
- authority                       - work contracts
- evidence                        - state/test contracts
- transitions                     - adapter contracts
- checkpoints                     - model migration
- reconstruction                  - repository classes
```

RTS is not expanded into a development runtime. The Development Kernel is not made part of RTS canonical history or runtime.

RTS itself, RTS-AGE, ecosystem components, and product repositories may be developed under the Kernel, but each remains separately owned and separately approved.

## 2. Complete architecture

```text
                         HUMAN PURPOSE / APPROVAL
                                   |
                                   v
                       RTS DEVELOPMENT KERNEL
        constitution / work / state / tests / evidence / limits
                                   |
                   +---------------+---------------+
                   |               |               |
                   v               v               v
              AI ADAPTER       TOOL ADAPTER    REPOSITORY ADAPTER
             model/provider    GitHub/shell     RTS/product/runtime
                   +---------------+---------------+
                                   |
                                   v
                                RTS-AGE
                   replaceable execution and preparation engine
                                   |
                            HUMAN AUTHORITY GATE
                                   |
              +--------------------+--------------------+
              |                    |                    |
              v                    v                    v
             RTS             ecosystem components     products
       trust/reconstruction    Hermes/Skills/etc.     derived software
```

## 3. Responsibility split

### RTS Trust Core

RTS owns:

- reconstructable decision structure;
- authority and approval records;
- evidence and integrity rules;
- state transitions;
- checkpoints and resume semantics;
- append-only or signed history;
- canonical RTS schema decisions.

RTS must remain reconstructable when the Development Kernel, RTS-AGE, a provider, an adapter, or an external tool is unavailable.

### RTS Development Kernel

The Kernel owns reusable rules for:

- locking purpose, scope, minimum success, and non-goals;
- preparing bounded work;
- recording compact execution state;
- separating automated and human tests;
- classifying evidence and uncertainty;
- limiting AI calls, retries, context, and active WIP;
- changing AI, tools, and execution software safely;
- stopping, rolling back, and reconstructing development;
- producing reviewable evidence packets for possible RTS recording.

The Kernel does not own product code, RTS canonical records, live deployment, customer action, or repository approval.

### RTS-AGE

RTS-AGE is a replaceable execution engine. It may:

- load an approved Kernel version;
- select approved adapters;
- prepare bounded work packets;
- execute authorized implementation and tests;
- return evidence and uncertainty packets.

RTS-AGE must not:

- approve its own work;
- create RTS authority;
- treat AI output as canonical automatically;
- rewrite signed history;
- merge, deploy, publish, pay, contact, or expand authority without a human gate.

### Adapters

Adapters translate stable Kernel contracts to replaceable software.

- AI Adapter: model/provider capabilities and limits.
- Tool Adapter: GitHub, shell, browser, CI, device, or other tool behavior.
- Repository Adapter: local repository class, allowed operations, evidence, and gates.

An adapter may restrict authority. It may never expand authority beyond the Kernel and local repository contract.

## 4. Dependency rule

### Development-time dependency

A repository may pin a reviewed Kernel version or commit while being developed.

### Runtime independence

The built or governed repository must not require the Kernel repository, an HTML view, a model provider, or RTS-AGE merely to run, inspect history, or reconstruct decisions unless a separately approved product requirement explicitly says otherwise.

### RTS special rule

```text
Development time: RTS may use the Kernel to prepare and verify proposals.
Operation/reconstruction time: RTS must remain independently usable.
```

This is a build-time procedure dependency, not a mandatory RTS runtime dependency.

## 5. Self-development and self-approval

The Kernel may be used to develop:

- the Kernel itself;
- RTS-AGE;
- adapters;
- RTS proposal changes;
- ecosystem components;
- products.

But no system may approve its own authority expansion.

```text
SELF_DEVELOPMENT_ALLOWED
SELF_TEST_ALLOWED
SELF_EVIDENCE_PREPARATION_ALLOWED
SELF_APPROVAL_PROHIBITED
SELF_MERGE_PROHIBITED
SELF_AUTHORITY_EXPANSION_PROHIBITED
```

Material Kernel changes require a human decision and a version change. RTS changes remain subject to RTS governance independently of Kernel approval.

## 6. Stable contracts

The Kernel consists of the following replaceable-but-versioned contract set:

1. Core Constitution
2. Work Contract
3. Project Contract
4. State Contract
5. Test Contract
6. Evidence Contract
7. Adapter Contract
8. Model Migration Contract
9. Repository Class Policy
10. Human Authority Contract

Stable inputs and outputs are preferred over provider-specific prompts or user interfaces.

## 7. Repository connection

Each connected repository receives only a thin local adapter such as:

```yaml
kernel:
  version: "1.0"
  commit: "<fixed-commit>"
repository:
  name: "RTS"
  class: "TRUST_CORE"
permissions:
  allowed:
    - inspect
    - propose
    - validate
    - test_on_isolated_branch
  prohibited:
    - direct_default_branch_write
    - self_approval
    - signed_history_rewrite
    - authority_expansion
required_evidence:
  - diff
  - test_results
  - rollback_point
  - uncertainty_report
  - human_approval
```

The central Kernel is not copied wholesale into each repository. Local product behavior and authority remain local.

## 8. Repository classes

Minimum classes:

- `SANDBOX`
- `COMPONENT`
- `PRODUCT`
- `RUNTIME`
- `GOVERNANCE`
- `TRUST_CORE`

RTS is `TRUST_CORE` with the maximum protection level. The class controls allowed operations, mandatory tests, human gates, and rollout order.

## 9. Replaceability target

The following must be replaceable without rewriting project purpose or evidence standards:

- AI model/provider;
- coding agent;
- orchestration engine;
- Git provider or repository tool;
- test runner;
- human-readable renderer;
- downstream product implementation.

Replacement occurs by changing an adapter/profile and passing compatibility tests. It does not silently change authority, minimum success, or canonical history.

## 10. Adoption sequence

```text
Kernel architecture approved
→ contract set completed
→ non-core sandbox adapter
→ forced interruption and reconstruction test
→ alternate AI/tool adapter test
→ component/product pilot
→ RTS-AGE integration review
→ RTS TRUST_CORE adapter proposal after RTS prerequisites
→ gradual opt-in rollout
```

No ecosystem-wide automatic mutation is authorized.

## 11. Current decision state

```text
TWO_FOUNDATIONAL_CORES_APPROVED_AS_DESIGN
RTS_REMAINS_TRUST_AND_RECONSTRUCTION_CORE
DEVELOPMENT_KERNEL_BECOMES_DEVELOPMENT_FOUNDATION
RTS_AGE_CLASSIFIED_AS_REPLACEABLE_EXECUTION_ENGINE
ADAPTER_BASED_SOFTWARE_REPLACEMENT_REQUIRED
BUILD_TIME_CONNECTION_ALLOWED
RTS_RUNTIME_DEPENDENCY_PROHIBITED_BY_DEFAULT
SELF_DEVELOPMENT_ALLOWED
SELF_APPROVAL_PROHIBITED
RTS_REPOSITORY_UNCHANGED
IMPLEMENTATION_CONTINUES_IN_DRAFT_PR
```