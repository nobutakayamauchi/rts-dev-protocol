# Human Authority Contract v1

Status: IMPLEMENTATION DRAFT  
Applies to: RTS Development Kernel, adapters, RTS-AGE, connected repositories

## 1. Principle

AI and software may prepare, implement, test, compare, and report. They may not manufacture human authority.

```text
AUTOMATION MAY PREPARE A DECISION
AUTOMATION MAY NOT BECOME THE DECISION HOLDER
```

## 2. Human-only decisions

A human decision is required before:

- changing purpose, minimum success, or material non-goals;
- changing repository class or reducing protection;
- approving an AI/tool/engine adapter for a new role;
- merging a material change to a protected or default branch;
- deploying or releasing to production;
- publishing or contacting an external party;
- making payment, contract, purchasing, or customer commitments;
- accessing real confidential or protected data;
- changing authority or governance semantics;
- modifying RTS canonical rules, signed records, FREEZER state, or checkpoints;
- expanding rollout to a new repository class.

## 3. Required approval record

A material approval should include:

```yaml
approval:
  decision_id: "<id>"
  approver: "<human identity or approved role>"
  decision: "APPROVE|APPROVE_WITH_LIMITS|REJECT|DEFER"
  scope: "<exact bounded scope>"
  project_hash: "<hash>"
  state_hash: "<hash>"
  tests_hash: "<hash>"
  evidence_packet: "<reference>"
  known_unknowns: []
  rollback_point: "<commit or recovery reference>"
  timestamp: "<time>"
```

A chat statement may establish implementation direction when explicitly recorded, but repository merge and any higher authority remain separate decisions.

## 4. Self-development boundary

A system may use the Kernel to modify itself on an isolated branch. It may run tests and prepare evidence about that change.

It may not:

- approve the change;
- classify its own evidence as human verified;
- merge the change;
- deploy the change;
- reduce its own protection level;
- expand its own authority.

## 5. Conflict rule

When instructions conflict, use this order:

1. safety and legal/data boundary;
2. human authority contract;
3. repository class policy;
4. local repository rules;
5. locked project and test contracts;
6. adapter instructions;
7. convenience or speed.

An adapter or execution engine cannot override a higher rule.

## 6. Missing or ambiguous approval

Missing, stale, mismatched, or ambiguous approval fails closed.

```text
NO APPROVAL RECORD
→ NO MERGE
→ NO DEPLOY
→ NO EXTERNAL ACTION
→ NO AUTHORITY CHANGE
```

## 7. RTS special protection

For `TRUST_CORE` repositories such as RTS:

- implementation direction and merge authorization are separate gates;
- proposal review and canonical adoption are separate gates;
- AI or RTS-AGE output is never canonical merely because tests pass;
- existing RTS governance remains authoritative over the proposal;
- Development Kernel approval does not equal RTS approval.
