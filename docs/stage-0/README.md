# Stage 0 Architecture Package

This package captures the first Stage 0 milestone for GeoHistory Explorer.

## Produced In This Milestone

- expanded top-level documentation
- repository scaffold with clear architectural boundaries
- initial Architecture Decision Records
- draft GeoHistory Pack manifest
- draft core schema
- evidence model
- precision model
- source and provenance model
- staged roadmap with Stage 1 acceptance criteria

## Stage 0 Scope

Stage 0 is architecture and repository foundation only. It should make future implementation safer, more inspectable, and more scientifically faithful.

Stage 0 should not build the full application, acquire authoritative production datasets, or introduce speculative AI workflows.

## Package Index

- [Evidence model](../models/evidence-model.md)
- [Precision model](../models/precision-model.md)
- [Source and provenance model](../models/source-provenance-model.md)
- [Stage 1 acceptance criteria](stage-1-acceptance-criteria.md)
- [Draft schema](../../schema/geohistory-pack.schema.json)
- [Draft manifest example](../../manifests/geohistory-pack.manifest.example.yaml)
- [Architecture Decision Records](../../ARCHITECTURAL_DECISIONS/)

## Review Questions

- Does the GeoHistory Pack correctly serve as the durable scientific object?
- Are the proposed pipeline boundaries clear enough?
- Does the evidence model keep source claims separate from derived observations?
- Does the precision model avoid inventing specificity?
- Does the provenance model attach enough context to derived artifacts?
- Are Stage 1 goals narrow enough for a toy pack?

## Milestone Boundary

This milestone stops at the Stage 0 architecture package. The next meaningful step should be review, amendment, or approval before Stage 1 toy-pack implementation begins.
