# Roadmap

GeoHistory Explorer is intentionally staged. Each stage should produce something useful and reviewable without assuming later stages will happen exactly as imagined.

## Stage 0 - Architecture And Repository Foundation

Status: **in progress**.

Goals:

- establish repository scaffold
- expand top-level project documentation
- draft schema and manifest structure
- define evidence model
- define precision model
- define source and provenance model
- create initial Architecture Decision Records
- define Stage 1 acceptance criteria

Non-goals:

- full application build
- production data acquisition
- speculative AI workflows
- polished viewer
- comprehensive domain ontology

First milestone:

- Stage 0 architecture package drafted under `docs/stage-0/`
- initial ADRs recorded under `ARCHITECTURAL_DECISIONS/`
- model drafts recorded under `docs/models/`
- schema and manifest drafts recorded under `schema/` and `manifests/`
- repository scaffold created without implementing a full application

Review gate:

Stage 0 should pause after the first architecture package for review. Amendments should be recorded in docs or ADRs before Stage 1 begins.

## Stage 1 - Toy GeoHistory Pack

Goals:

- create a small public or synthetic toy historical seismology pack
- validate the draft schema against toy records
- produce a deterministic build path
- export a GeoPackage
- export a human-readable summary
- generate a QA report

Acceptance criteria are drafted in [docs/stage-0/stage-1-acceptance-criteria.md](docs/stage-0/stage-1-acceptance-criteria.md).

Stage 1 should use toy or public sample data only. It should prove the architecture without pretending to solve authoritative historical seismology.

## Stage 2 - Deterministic Query Layer

Candidate goals:

- evidence-grounded search and filtering
- spatial and temporal query primitives
- disagreement-aware query results
- provenance-preserving derived views

This stage should remain deterministic before any natural-language layer is considered.

## Stage 3 - Explorer Prototype

Candidate goals:

- inspect GeoHistory Packs visually
- compare source claims and normalized observations
- surface uncertainty, precision, and provenance clearly
- remain downstream from pack storage

## Stage 4 - Community Packs And Extensions

Candidate goals:

- pack authoring guidance
- validation profiles
- stable extension points
- domain-specific pack conventions

## Deferred Until Explicit Approval

- production-scale ingestion
- authoritative catalog reconciliation
- AI-assisted interpretation workflows
- plugin marketplace or broad extension system
- full public web application
