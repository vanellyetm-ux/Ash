# GHOST–OLPIRT intake for Ash

## Scope

This directory defines the repository-side intake contract for structured knowledge records. It does not claim a live connection to a physical device, remote service, or AshShow organization repository.

## Required intake sequence

1. Capture the source reference and immutable revision where available.
2. Compute and retain a SHA-256 digest of the source payload.
3. Classify the payload as observation, interpretation, proposal, or question.
4. Preserve original text separately from normalized or generated text.
5. Validate the record against the schema in `schemas/knowledge-record.schema.json`.
6. Attach scoped authorization before any repository write.
7. Write only to a dedicated feature branch.
8. Read back the destination file and verify both commit identity and content digest.
9. Request human evidence review and promotion approval.

## Destination routing

- **Ash** — supported by this repository PR as the structured knowledge destination.
- **$ilk mirror** — transport/provenance companion repository.
- **Lumi** — narrative and knowledge presentation companion repository.
- **AshShow/V** — external destination. This repository stores the destination identity and handoff requirements only; it does not attempt an AshShow write.

## Required transfer receipt

A receipt should include the source repository/ref/commit/path/digest, destination repository/ref/path, authorization identifier and approved scope, resulting commit, readback digest, and verification result.

## Safety boundary

- No force-push or default-branch write is part of this workflow.
- No credentials or private keys belong in source files or receipts.
- A local unit test is not proof of remote connectivity.
- A generated record is not automatically an observed fact.
- A successful write is not equivalent to evidence approval or publication.
