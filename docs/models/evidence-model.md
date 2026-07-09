# Evidence Model

The evidence model separates source-grounded statements from derived observations. It is designed to preserve uncertainty, disagreement, and stated precision while allowing later deterministic exports.

## Model Layers

### Source

A source is the material basis for evidence. It may be a chronicle, archive item, catalog, field report, article, map, dataset, translation, database extract, or other citable object.

Sources describe where evidence comes from. They do not by themselves assert a normalized event.

### Evidence Record

An evidence record preserves one source-grounded statement, observation, or structured claim.

Evidence records should retain:

- source identifier
- source locator, such as page, folio, row, entry, URL fragment, or map sheet
- original expression when legally and practically possible
- transcription or translation notes where relevant
- temporal claim with precision
- spatial claim with precision
- measurement or qualitative claim with precision
- uncertainty notes
- rights or access limitations affecting reuse

Evidence records should not be forced to agree with one another.

### Derived Observation

A derived observation is produced from one or more evidence records. It may normalize place, time, phenomenon type, measurement scale, or other analytical fields.

Derived observations must retain:

- supporting evidence identifiers
- derivation method
- transformation version or process identifier
- assumptions introduced during derivation
- validation warnings
- precision changes, if any

Derived observations are useful for querying and export, but they remain downstream from evidence.

## Disagreement Pattern

When sources disagree, represent separate evidence records and, if needed, separate derived observations. Do not overwrite disagreement with a single preferred claim during Stage 0 or Stage 1.

A later synthesis may identify a working interpretation, but it must be marked as derived, cite its supporting evidence, and remain reversible.

## Minimal Stage 1 Test

The Stage 1 toy pack should include at least one case where two evidence records describe the same broad phenomenon with different temporal or spatial precision. This will test whether the model preserves disagreement without inventing specificity.

## Architectural Decision

Chosen approach: source, evidence, and derived observation remain distinct layers.

Reason: this keeps original claims inspectable and makes later transformations auditable.

Viable alternative: model only normalized events with citations back to sources.

Reason deferred: event-first modeling is easier for maps and simple search, but it collapses source texture too early and makes disagreement harder to preserve.

Cost to change later: high once packs, validation rules, and exports depend on the layer boundaries.
