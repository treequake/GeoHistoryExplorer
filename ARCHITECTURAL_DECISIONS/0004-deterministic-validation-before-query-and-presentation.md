# ADR 0004: Put Deterministic Validation Before Query And Presentation

Status: Accepted for Stage 0 draft

Date: 2026-07-09

## Decision

GeoHistory Explorer will require deterministic pack validation and export checks before investing in query layers, presentation layers, or AI-assisted interpretation.

## Reasoning

The durable scientific object is the GeoHistory Pack. Query tools and interfaces are useful only if the pack can first be inspected, validated, and exported through reproducible processes.

Historical Earth-system evidence contains uncertainty, disagreement, and uneven precision. Deterministic validation makes those qualities visible without resolving them prematurely.

## Alternatives Considered

- Build a viewer first and validate only the fields needed for display.
- Build a natural-language or AI-assisted query layer early to accelerate exploration.
- Treat validation as informal documentation until production data exists.

## Why Alternatives Were Rejected Or Deferred

A viewer-first approach risks letting presentation constraints reshape evidence storage. Early natural-language or AI-assisted query would sit too close to interpretation before source-grounded structures are stable. Informal validation is insufficient for a pack intended to remain inspectable and reproducible over decades.

## Consequences

Stage 1 should prioritize schema validation, QA reporting, deterministic GeoPackage export, and summary export. Query and presentation remain downstream consumers until the pack format has been exercised with a toy example.

## Cost To Change Later

Medium. The sequencing can be revisited after Stage 1, but skipping deterministic validation early would make later correction more expensive because examples, exports, and user expectations would already depend on unverified assumptions.
