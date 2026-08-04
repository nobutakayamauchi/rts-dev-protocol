# Development Protocol Inventory

Status: DRAFT / REVIEW REQUIRED

This inventory is documentation-only. It does not change RTS authority, runtime behavior, deployment, product behavior, or external actions.

## Classification rules

- `READY`: safe to use as a reviewed development procedure.
- `DRAFT`: useful but requires human review before adoption.
- `RISKY`: may affect authority, runtime, deployment, secrets, customers, or multiple repositories.
- `BLOCKED`: must not proceed until a named prerequisite is complete.
- `DERIVED`: non-authoritative presentation generated from or summarizing another source.

## Inventory

| Item | Path | Status | Applies to | Risk | Next smallest safe action |
|---|---|---|---|---|---|
| AI-efficient development protocol | `docs/contracts/AI_EFFICIENT_DEVELOPMENT_PROTOCOL_V1.md` | DRAFT | all repository classes | medium | review principles and acceptance gates |
| RTS adoption contract | `docs/contracts/RTS_ADOPTION_CONTRACT_DRAFT_V1.md` | BLOCKED | RTS trust and reconstruction core | high | complete RTS Stage 2 classification/reference analysis first |
| Model migration policy | `docs/policies/MODEL_MIGRATION_POLICY_V1.yaml` | DRAFT | AI-assisted development | medium | run compatibility benchmark before changing primary AI |
| Project adapter template | `templates/PROJECT.template.yaml` | DRAFT | product/component repositories | low | pilot in one non-core repository |
| State adapter template | `templates/STATE.template.yaml` | DRAFT | product/component repositories | low | verify reconstruction after forced interruption |
| Test adapter template | `templates/TESTS.template.yaml` | DRAFT | product/component repositories | low | bind every claim to a test/evidence ID |
| Human-readable HTML view | `docs/html/AI_EFFICIENT_DEVELOPMENT_PROTOCOL_V1.html` | DERIVED | operators and reviewers | low | review visually; do not treat as canonical authority |

## Repository-class boundary

### RTS

RTS is the trust and reconstruction core. No automatic adoption, authority expansion, schema replacement, history rewrite, FREEZER mutation, runtime change, or cross-repository rollout is authorized by this inventory.

### RTS-AGE

RTS-AGE may later consume approved contracts and prepare execution artifacts. It must not manufacture approval or canonical RTS records.

### rts-dev-protocol

This repository owns reusable development procedures, AI implementation contracts, review checklists, and migration guidance. It does not own RTS canonical records or runtime execution.

### Product and component repositories

These repositories may later receive a thin adapter after the protocol is reviewed. They retain ownership of product-specific code and behavior.

## Stop conditions

Stop and require human review if work would:

- change RTS authority or canonical record semantics;
- rewrite signed or append-only history;
- bypass FREEZER, preflight, checkpoint, or human approval;
- add deployment, external contact, payment, publication, or customer action;
- expose credentials, private data, or protected information;
- apply a draft protocol ecosystem-wide;
- update multiple repositories without per-repository evidence and rollback plans.
