# GeoHistory Explorer

GeoHistory Explorer is an open, extensible scientific instrument for exploring historical Earth-system evidence.

The project begins with historical seismology, but the core architecture is intended to support future historical Earth-system domains without redesigning the evidence model.

Read [VISION.md](VISION.md) first. Then read [ARCHITECTURE.md](ARCHITECTURE.md), [ROADMAP.md](ROADMAP.md), and the Stage 0 architecture package under [docs/stage-0/](docs/stage-0/).

## Stage

Current stage: **Stage 0 - architecture and repository foundation**.

Stage 0 does not build the full application. It establishes the repository structure, evidence model, provenance expectations, precision rules, and staged implementation path needed before executable work begins.

## Core Commitments

- Preserve original source information.
- Preserve provenance, uncertainty, and disagreement.
- Never invent temporal or spatial precision.
- Keep presentation separate from stored evidence.
- Keep AI downstream from deterministic, source-grounded evidence.
- Design each stage so it is useful on its own.

## Stage 0 Package

The first Stage 0 architecture package contains:

- [Stage 0 package summary](docs/stage-0/README.md)
- [Stage 1 acceptance criteria](docs/stage-0/stage-1-acceptance-criteria.md)
- [Evidence model](docs/models/evidence-model.md)
- [Precision model](docs/models/precision-model.md)
- [Source and provenance model](docs/models/source-provenance-model.md)
- [Draft GeoHistory Pack schema](schema/geohistory-pack.schema.json)
- [Draft manifest example](manifests/geohistory-pack.manifest.example.yaml)
- [Architecture Decision Records](ARCHITECTURAL_DECISIONS/)

## Repository Map

- `VISION.md` - long-lived scientific purpose and project boundaries.
- `ARCHITECTURE.md` - core components and data flow.
- `ROADMAP.md` - staged development plan.
- `ARCHITECTURAL_DECISIONS/` - numbered architecture decision records.
- `docs/models/` - precision, provenance, source, and evidence model drafts.
- `docs/stage-0/` - Stage 0 package summary and review notes.
- `schema/` - repository-ready schema drafts.
- `manifests/` - GeoHistory Pack manifest drafts and examples.
- `src/geohistory/` - future implementation scaffold separated by pipeline boundary.
- `packs/` - future pack examples, beginning with toy Stage 1 data only.
- `tests/` - future validation and regression tests.

## Near-Term Work

Stage 0 should remain focused on inspectable architecture. Stage 1 may introduce a toy GeoHistory Pack, deterministic build path, GeoPackage export, summary export, and QA report using public or sample data only.
