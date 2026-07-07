# rts-dev-protocol Status

Status: PARTS / DEV-PROTOCOL / INVENTORY NEEDED

rts-dev-protocol is the development protocol and AI implementation procedure shelf for the RTS ecosystem.

It is a component repository, not RTS core.

It is not RTS-AGE.

It is not a runtime implementation repository.

It is not a product repository.

It is not a business workflow repository.

## Current Position

This repository should hold reusable development procedures that help AI-assisted work remain reviewable, scoped, and reversible.

Its purpose is to define how work should be prepared, constrained, reviewed, and handed off across RTS-related repositories.

Allowed by default:

- document AI implementation contracts
- add PR review checklists
- add repository rescue procedures
- document Codex task boundaries
- document safe branch, PR, and merge patterns
- document review-first and rollback-cheap development procedures
- separate facts, assumptions, unverified material, risks, and open questions

Prohibited by default:

- adding product implementation code
- adding runtime implementation code
- adding RTS core canonical records
- adding secrets or credentials
- adding connector implementation
- adding business delivery workflows
- turning this repository into RTS-AGE
- turning this repository into a deployment system
- broad refactors without an inventory decision

## Boundary

RTS defines the protocol and canonical reconstructability rules.

RTS-AGE may execute or prepare implementation artifacts.

Product repositories own their product-specific code and delivery behavior.

Component repositories own their own manifests, drives, packs, skills, and design material.

rts-dev-protocol should define development procedure and review discipline across those repositories without absorbing their implementation details.

## Minimum Alive Definition

This repository is considered Minimum Alive when:

1. Its role as a development protocol shelf is explicit.
2. Its boundaries from runtime, product, protocol, and business repositories are clear.
3. Its next inventory pass is documented.
4. It can guide AI-assisted development without becoming an execution system.
5. No runtime behavior, product behavior, or canonical RTS data is changed by the rescue documentation itself.

## Current Decision

Keep this repository.

Treat it as a parts shelf for RTS-compatible development protocol, AI implementation contracts, and review procedures.

Do not expand it into runtime, product, deployment, or business workflow implementation without a separate decision record.
