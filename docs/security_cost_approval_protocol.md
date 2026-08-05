# Security → Cost → Approval Development Protocol

Status: REVIEW-REQUIRED DEVELOPMENT PROCEDURE

This procedure applies when development work can ingest untrusted content, invoke paid services, mutate external systems, publish material, or execute consequential actions.

## Required order

```text
1. Inspect and constrain input
2. Produce SECURITY_PASS bound to an input hash
3. Estimate cost and operational consequence
4. Display the bounded execution envelope
5. Obtain explicit single-use approval
6. Execute exactly once within that envelope
7. Verify output and record the outcome
```

Skipping or reordering the gates is a protocol failure.

## Security inspection

Inspect all relevant surfaces: media, documents, archives, structured data, filenames, paths, metadata, manifests, prompts, URLs, environment references, and command arguments.

Required controls:

- allowlisted formats and schemas
- actual MIME/structure verification
- size, duration, resolution, stream, recursion, and decompression limits
- path normalization and internally generated names
- no shell interpolation of untrusted values
- prompts and manifests treated as untrusted data
- active content and unnecessary metadata removed
- decoders/probes isolated, least-privileged, network-restricted, and timeout-bounded
- accepted media re-encoded into a constrained representation where practical
- ambiguous or uninspectable content quarantined or rejected
- downstream approval bound to the inspected content hash

## Cost and consequence estimate

After SECURITY_PASS, calculate and show:

- provider, account/project, region, and operation
- resource size, model/API, CPU, memory, accelerator, runtime, parallelism, and retries
- input/output transfer and retention assumptions
- maximum monetary estimate or a reason execution must stop
- external side effects, publication, or mutation
- cancellation, rollback, and cleanup behavior

Conservative defaults are mandatory: one task, no automatic retry, bounded runtime, bounded input, and no paid automatic fallback.

## Approval

Approval must be explicit, time-limited, single-use, parameter-bound, provider-bound, and hash-bound. A changed input, command, provider, limit, or consequence invalidates the approval.

## Execution

Execution code must enforce the envelope. Operator habit is not a control.

- prevent duplicate paid execution
- reject widened parameters
- do not add retries or parallelism
- do not publish or mutate externally unless separately approved
- stop on security or cost-state mismatch

## Audit record

Record the Security Gate result, hashes, estimate, approval, exact parameters, provider job identifier, duration, output verification, known cost, cleanup, and deviations.

## Emergency overflow compute

Overflow compute used because the primary environment lacks capacity is exceptional, manually selected, and never an automatic default. It still requires the complete gate sequence for every execution.
