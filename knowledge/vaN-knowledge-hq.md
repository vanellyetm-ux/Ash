# VaN Knowledge HQ

## Purpose

VaN Knowledge HQ is the structured stewardship layer for knowledge arriving through the OLPIRT and GHOST workflow. It preserves what was observed, how it was interpreted, what was proposed, and what remains uncertain.

## Source-to-knowledge flow

1. **OLPIRT / origin** — retain the original source, author or system, timestamp, and immutable source reference where available.
2. **BOF / foundation** — classify the incoming material as observation, interpretation, proposal, or question.
3. **GHOST** — translate the source into a structured transfer record without erasing the original wording or lineage.
4. **$ilk mirror** — retain a provenance-preserving transport copy and transfer receipt.
5. **Ash** — curate structured knowledge records, evidence, relationships, and review state.
6. **AshShow/V** — optional downstream narrative presentation. AshShow is external to this repository and is not required for this PR.

## Knowledge domains

- **$ilk / Vœ** — mirror identity, transfer lineage, and provenance.
- **GHOST** — local gateway, translation, validation, and transfer-envelope handling.
- **OLPIRT** — origin narratives and source context.
- **BOF** — maturation, mitigation, classification, and evidence development.
- **AshShow/V** — downstream presentation target; external authorization required for any write.
- **Ash** — structured knowledge and stewardship records.
- **Git Freedom Bridge** — branch, review, and promotion workflow.
- **PONS / evidence governance** — scoped authorization, independent evidence review, and auditable decisions.

## Record rules

- Preserve original source text and source references.
- Separate observation from interpretation and proposal.
- Keep confidence and uncertainty explicit.
- Never convert a simulation, generated fixture, or local test into a claim of physical or remote execution.
- Do not store credentials, private keys, access tokens, or passwords in knowledge records.
- Do not overwrite historical records; issue a superseding record with a link to the prior record.
- Keep default-branch changes behind review and merge authorization.

## Promotion ladder

`DRAFT` → `SOURCE_VERIFIED` → `EVIDENCE_REVIEWED` → `IMPLEMENTATION_VERIFIED` → `PROMOTION_APPROVED` → `PUBLISHED`

Each transition requires an attributable decision. A transfer receipt proves only that a transfer was acknowledged; it does not prove correctness, evidence quality, or publication.

## AshShow boundary

This repository records AshShow/V as a downstream destination only. The current integration does not create files, branches, releases, or PRs in the AshShow organization. A future AshShow delivery must use an organization-authorized integration or a human-operated import, followed by readback verification.
