# RTS Development Kernel — Next Actions

The architecture direction is approved. The next work is bounded contract completion and non-core validation, not ecosystem-wide rollout.

## Current sequence

1. Review the Kernel architecture and Core Constitution for internal contradictions.
2. Validate YAML syntax and required-field consistency across contracts/templates.
3. Complete the thin repository-adapter template.
4. Update the derived read-only HTML view.
5. Keep Draft PR reviewable; do not merge automatically.
6. Select one non-core sandbox repository.
7. Add only a version-pinned thin adapter and local PROJECT/STATE/TESTS files.
8. Run one bounded no-runtime-change task.
9. Force an interruption and reconstruct from STATE in another AI/chat.
10. Run the same compatibility surface with an alternate AI or tool adapter.
11. Compare usage, scope drift, evidence quality, rollback, and restart success.
12. Approve, revise, or reject expansion to the next repository class.

## Rollout order

```text
SANDBOX
→ COMPONENT
→ PRODUCT
→ RUNTIME
→ GOVERNANCE
→ TRUST_CORE
```

Each repository receives its own branch, evidence, rollback point, and human decision. No automatic cross-repository synchronization or mutation is permitted.

## RTS boundary

RTS is `TRUST_CORE` and is last in rollout order.

Before an RTS proposal:

- RTS Stage 2 classification/reference analysis must be complete;
- candidate paths and overlapping semantics must be reviewed;
- a fixed RTS base commit and rollback must be recorded;
- a human must authorize Gate A (isolated proposal only);
- read-only/fail-closed tests and byte-invariance checks must pass;
- a second human decision must authorize merge/canonical adoption.

Kernel approval does not equal RTS approval.

## Validation checklist for this Draft PR

- [ ] all Markdown links point to existing branch files;
- [ ] YAML files parse successfully;
- [ ] required statuses and authority fields are consistent;
- [ ] old “RTS adoption” framing is absent;
- [ ] RTS is represented as a development-time `TRUST_CORE` adapter;
- [ ] RTS runtime/reconstruction independence is explicit;
- [ ] self-development is allowed but self-approval is prohibited;
- [ ] HTML is derived, self-contained, and network-free;
- [ ] no runtime, product, deployment, secret, customer, or canonical RTS behavior is added;
- [ ] the PR remains Draft until human review.

## Do not do yet

- do not modify RTS;
- do not implement RTS-AGE runtime behavior;
- do not deploy a synchronization service;
- do not copy the Kernel wholesale into connected repositories;
- do not mutate multiple repositories in one operation;
- do not merge or mark the Draft ready automatically;
- do not treat test success as human approval.

## Next bounded implementation task

Complete and validate the Kernel Draft PR, then prepare one `SANDBOX` pilot adapter proposal. Stop before modifying the sandbox until the Draft contract review is complete.
