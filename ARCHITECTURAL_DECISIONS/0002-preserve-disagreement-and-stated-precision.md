# ADR 0002: Preserve Disagreement And Stated Precision

Status: Accepted for Stage 0 draft

Date: 2026-07-09

## Decision

The core model will preserve disagreement and stated precision instead of collapsing evidence into a single preferred date, location, geometry, intensity, magnitude, or interpretation.

## Reasoning

Historical Earth-system evidence is often fragmentary and conflicting. Scientific usefulness depends on being able to inspect what sources claim, what precision they state, and how later transformations interpret those claims.

The model must not invent exact coordinates, dates, or confidence when the source does not provide them.

## Alternatives Considered

- Require each event or observation to have one canonical best estimate.
- Store uncertainty only as free-text notes.
- Normalize all records to precise modern geometry and timestamps.

## Why Alternatives Were Rejected Or Deferred

A single best estimate hides disagreement and makes later audit difficult. Free-text uncertainty is useful for human context but weak for validation and deterministic export. Forced precision creates false scientific confidence.

## Consequences

Schemas need explicit precision and uncertainty fields. Queries and exports must handle multiple claims for what may appear to be the same phenomenon. Interfaces must make uncertainty visible rather than smoothing it away.

## Cost To Change Later

High. If early records collapse disagreement, lost distinctions may not be recoverable.
