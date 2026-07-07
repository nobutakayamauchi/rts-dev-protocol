# AGENTS.md

## Scope

This file applies to the entire repository.

## Required reading

Before editing, read:

1. `README.md`
2. `docs/STATUS.md`
3. `docs/NEXT.md`

## Repository guardrails

- Keep this repository as the RTS development protocol and AI implementation procedure shelf.
- Do not add product implementation code by default.
- Do not add runtime implementation code by default.
- Do not add deployment automation by default.
- Do not import RTS core canonical records.
- Do not import RTS-AGE implementation internals.
- Do not add secrets, API keys, credentials, or live external action material.
- Do not present draft procedures as mandatory ecosystem-wide rules without review.
- Prefer implementation-neutral development procedures over broad automation changes.

## Inventory pass boundary

- Treat the next pass as development protocol inventory and risk review, not implementation expansion.
- Prefer adding or improving index, inventory, checklist, and boundary documentation before changing protocols.
- Do not promote a development protocol to mandatory ecosystem-wide status without a separate review decision.
- If a protocol implies direct deployment, live mutation, customer contact, secret handling, or broad repository changes, mark it as `RISKY` in inventory documentation instead of expanding it immediately.
- If a protocol belongs in another repository, mark it as `MOVE` instead of moving it immediately.

## Documentation rules

- Separate confirmed facts, assumptions, unverified material, risks, and open questions.
- Record applicable repository class for each protocol when possible.
- Keep procedures reviewable, scoped, and rollback-cheap.
- Use minimal additive edits over broad refactors.

## Validation

- Check for broken local doc links when adding index or onboarding docs.
- For documentation-only changes, report changed files and confirm that no runtime, product, deployment, secret, customer-contact, or canonical RTS data implementation was added.
