# rts-dev-protocol Next Actions

The next goal is an inventory pass, not implementation expansion.

## Next Tasks

1. List existing development procedures, prompts, checklists, and protocol notes.
2. Identify which materials are ready, draft, stale, duplicate, risky, or misplaced.
3. Confirm which procedures apply globally and which are repository-specific.
4. Separate facts, assumptions, unverified material, risks, and open questions.
5. Convert useful patterns into implementation-neutral development protocols.
6. Check local documentation links.
7. Decide which development protocol materials should remain here and which belong in adjacent repositories.

## Suggested Follow-up Files

```text
docs/inventory/dev_protocol_inventory.md
docs/contracts/implementation_contract.md
docs/checklists/pr_review_checklist.md
docs/relations/adjacent_repo_boundaries.md
```

## Inventory Categories

Use these labels during the next pass:

- READY: usable as reusable development protocol
- DRAFT: useful but incomplete
- STALE: likely outdated or superseded
- DUPLICATE: overlaps another protocol or checklist
- RISKY: could change runtime, product, deployment, or business behavior if followed blindly
- MOVE: belongs in another repository
- ARCHIVE: preserve for history only

## Development Protocol Review Checklist

Each development protocol item should explicitly describe:

- name
- path
- purpose
- applicable repositories
- required inputs
- allowed outputs
- prohibited actions
- review requirement
- rollback note
- next smallest safe action

If a protocol implies direct deployment, live mutation, customer contact, secret handling, or broad repository changes, mark it as `RISKY` and do not expand it until reviewed.

## Do Not Do Yet

Do not:

- add product implementation code
- add runtime execution code
- add deployment automation
- add secrets, API keys, or credentials
- import canonical RTS records
- rewrite all development procedures at once
- promote a protocol to mandatory ecosystem-wide status without review

## Next Recommended Task

Create `docs/inventory/dev_protocol_inventory.md`.

That file should list each known development procedure or checklist with:

1. name
2. path
3. purpose
4. status label
5. applicable repo or repo class
6. required inputs
7. allowed outputs
8. risk
9. next smallest safe action
