# ADR 0001: Treat GeoHistory Pack As The Durable Scientific Object

Status: Accepted for Stage 0 draft

Date: 2026-07-09

## Decision

GeoHistory Explorer will treat the GeoHistory Pack as the durable scientific object. Applications, viewers, notebooks, QGIS projects, AI summaries, and other tools are downstream consumers of the pack.

## Reasoning

The project exists to preserve and inspect historical Earth-system evidence. A durable pack keeps source records, evidence items, normalized observations, exports, validation results, and provenance together in a form that can outlive any one interface.

This supports reproducibility, long-term curation, and independent inspection by researchers using different tools.

## Alternatives Considered

- Make the Explorer application the primary system of record.
- Store evidence primarily in a hosted database.
- Treat exports, such as GeoPackage, as the canonical object.

## Why Alternatives Were Rejected Or Deferred

An application-centered architecture would make preservation depend too heavily on a particular interface. A hosted database may become appropriate later, but it is not a stable archival unit by itself. GeoPackage is valuable as an export, but it cannot carry the complete source, provenance, disagreement, validation, and build context as flexibly as a pack.

## Consequences

The repository must define pack layout, manifests, validation expectations, and provenance rules before building rich viewers. This slows visible feature work but strengthens scientific durability.

## Cost To Change Later

High. Changing the durable object later would affect schemas, exports, validation, documentation, and user expectations.
