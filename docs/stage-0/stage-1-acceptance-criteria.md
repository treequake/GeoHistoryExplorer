# Stage 1 Acceptance Criteria

Stage 1 should prove the Stage 0 architecture with a toy GeoHistory Pack. It should not become a production data project or a full application build.

## Required Outcomes

Stage 1 is acceptable when the repository can demonstrate:

- a small toy pack using public sample data or synthetic examples
- at least two source records
- at least three evidence records
- at least one preserved disagreement or precision mismatch
- a valid pack manifest
- schema validation against the Stage 0 draft schema
- a deterministic build command or documented build procedure
- GeoPackage export suitable for basic GIS inspection
- human-readable summary export
- QA report listing validation status, warnings, and known limitations

## Scientific Integrity Checks

The toy pack must demonstrate that:

- source claims remain visible after normalization
- derived observations cite supporting evidence records
- temporal and spatial precision are not silently upgraded
- disagreement remains represented rather than collapsed
- exports carry enough provenance to be audited

## Non-Goals

Stage 1 should not attempt:

- authoritative historical seismology coverage
- production-scale ingestion
- a polished Explorer interface
- natural-language querying
- AI-assisted interpretation
- plugin architecture

## Review Questions Before Stage 2

Before leaving Stage 1, reviewers should be able to answer:

- Can a researcher inspect the pack without trusting a custom viewer?
- Can every derived object be traced back to source evidence?
- Did the GeoPackage export lose any important uncertainty or disagreement?
- Are validation warnings understandable and useful?
- Is the next stage blocked by data model gaps rather than feature appetite?

## Architectural Decision

Chosen approach: Stage 1 success is defined by a toy pack plus deterministic exports and QA, not by application features.

Reason: this tests whether the pack is useful as a durable scientific object before presentation work begins.

Viable alternative: build a minimal Explorer interface first and backfill pack validation later.

Reason deferred: interface-first work would create pressure to simplify evidence for display and could make presentation needs drive the core model.

Cost to change later: medium. Stage boundaries can be adjusted, but once implementation begins, acceptance criteria will shape tests, examples, and review expectations.
