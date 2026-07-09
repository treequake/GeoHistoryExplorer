# ADR 0003: Separate Ingestion, Normalization, Storage, Export, Query, And Presentation

Status: Accepted for Stage 0 draft

Date: 2026-07-09

## Decision

The repository and future implementation will keep ingestion, normalization, storage, export, querying, and presentation as separate architectural boundaries.

## Reasoning

Each stage should be inspectable and useful on its own. Separating boundaries prevents presentation needs from reshaping evidence storage, and it makes deterministic transformations easier to test and audit.

## Alternatives Considered

- Build a single integrated application first.
- Combine normalization and storage in one implicit database layer.
- Let the viewer define the working data model.

## Why Alternatives Were Rejected Or Deferred

An integrated application would move too quickly toward feature breadth. Combining layers would obscure where source claims become derived observations. A viewer-defined model would risk making presentation the source of truth.

## Consequences

The repository scaffold includes empty implementation areas for each boundary even though Stage 0 does not implement them. Later stages should add code only where the stage requires it.

## Cost To Change Later

Medium to high. Boundary changes are possible while the repository is young, but they become expensive once schemas, tests, exports, and pack examples depend on them.
