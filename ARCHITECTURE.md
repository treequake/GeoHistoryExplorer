# Architecture

GeoHistory Explorer is organized around durable, inspectable **GeoHistory Packs**. A pack contains source records, evidence records, derived observations, exports, manifests, validation results, and provenance metadata.

The architecture is intentionally stage-based. Stage 0 defines the repository foundation and evidence model. Stage 1 proves the model with a toy pack and deterministic exports. Later stages may add richer query and presentation layers only after the pack format is useful on its own.

## Core Components

### GeoHistory Pack

The GeoHistory Pack is the durable scientific object. It must be usable without any one viewer or service.

A pack should contain:

- source descriptions and citation metadata
- evidence records transcribed or referenced from sources
- normalized observations derived from evidence
- explicit temporal and spatial precision metadata
- preserved disagreement between sources or interpretations
- deterministic export artifacts
- QA reports and validation results
- a manifest describing contents, build process, versions, and limitations

### Evidence Model

The model separates source descriptions, source-grounded evidence records, and derived observations.

This separation is architectural, not cosmetic. It prevents normalized observations and exports from replacing the original evidentiary claims they depend on.

See [docs/models/evidence-model.md](docs/models/evidence-model.md).

### Engine

The engine is a deterministic processing pipeline that validates, normalizes, links, and exports pack contents. It should be boring, inspectable, testable, and modular.

Pipeline boundaries:

- ingestion: accept source-grounded records without altering claims
- normalization: map evidence into shared concepts while preserving originals
- storage: maintain canonical pack layout and validation state
- export: produce downstream formats such as GeoPackage and summaries
- querying: provide deterministic evidence-grounded access patterns
- presentation: visualize or inspect packs without becoming the source of record

### Explorer

The Explorer is a downstream presentation layer. It may help users inspect a pack, compare evidence, and navigate uncertainty, but it must not become the canonical store of evidence.

### Plugins

Plugins are deferred until the core pack and engine boundaries are stable. Non-core capabilities should remain outside the core architecture unless they directly expand inspectable evidence handling.

### AI Summaries

AI may be useful downstream for summarization or assistance, but it must not sit upstream of deterministic source-grounded evidence. AI outputs must be clearly marked as derived interpretation and must cite the evidence objects they summarize.

## Data Flow

1. Sources are described with stable identifiers, citation metadata, rights notes, and access notes.
2. Evidence records preserve source-grounded statements and original precision.
3. Normalized observations are derived from evidence records with explicit transformation provenance.
4. Disagreements remain represented as separate claims or interpretations.
5. Exports are generated deterministically from pack contents.
6. QA reports document validation status, warnings, and known limitations.

## Stage 0 Repository Scaffold

The repository separates vision, architecture, documentation, schema drafts, future code, and future example packs:

```text
ARCHITECTURAL_DECISIONS/
docs/
  models/
  stage-0/
schema/
manifests/
src/geohistory/
  ingestion/
  normalization/
  storage/
  export/
  query/
  presentation/
packs/
  toy/
tests/
```

The `presentation` scaffold exists to preserve a boundary, not to begin application work during Stage 0.

## Architectural Decisions

Major decisions are recorded in [ARCHITECTURAL_DECISIONS/](ARCHITECTURAL_DECISIONS/). Each ADR must explain the chosen approach, viable alternatives, rejection or deferral reasoning, and likely cost of changing the decision later.
