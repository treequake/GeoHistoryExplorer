# Source And Provenance Model

The source and provenance model keeps evidence traceable from original source material through every derived object and export.

## Source

A source describes a work, archival item, dataset, catalog, map, report, article, translation, database extract, or other material from which evidence is taken.

Minimum source fields:

- stable source identifier
- title or short label
- creator, compiler, or responsible organization when known
- date or date range when known
- citation text
- source type
- language when known
- rights and access notes
- repository, URL, DOI, archive reference, or catalog reference when available
- reliability or scope notes where appropriate

## Evidence Record

An evidence record preserves a source-grounded statement or observation.

Minimum evidence fields:

- stable evidence identifier
- source identifier
- source location, such as page, folio, row, URL fragment, or catalog entry
- original text, transcription, quotation, or structured source value when available and rights allow
- language and translation notes when applicable
- observed phenomenon or claim type
- temporal claim with precision
- spatial claim with precision
- measurement or qualitative claim with precision
- uncertainty and interpretation notes

## Derived Observation

A derived observation is a normalized or interpreted object produced from one or more evidence records.

Minimum derived observation fields:

- stable observation identifier
- observation type
- source evidence identifiers
- normalized temporal representation
- normalized spatial representation
- normalized measurements or classifications
- derivation method
- transformation version
- responsible actor or process
- generated timestamp
- known limitations

## Provenance Chain

Every derived object should answer:

- What source records support this?
- What transformation produced it?
- What precision was preserved or changed?
- What assumptions were introduced?
- What validation warnings apply?

## Disagreement

Disagreement should be represented by multiple claims or observations linked to their evidence, not erased by a preferred value. A later synthesis may designate a working interpretation, but that interpretation must remain derived and reversible.

## Exports

Every export artifact should include:

- source pack identifier and version
- generation command or process name
- schema version
- generation timestamp
- included records
- validation status
- warnings and omissions
