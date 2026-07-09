# Precision Model

The precision model records what a source or transformation actually supports. It must never imply exactness that the evidence does not provide.

## Principles

- Record original stated precision.
- Separate original source claims from normalized values.
- Represent temporal and spatial uncertainty explicitly.
- Preserve qualitative uncertainty notes alongside structured fields.
- Allow multiple incompatible claims to coexist.

## Temporal Precision

Temporal values should distinguish:

- exact instant
- date
- month
- year
- interval
- approximate interval
- relative expression from source
- unknown or unstated

Examples:

- `1857-12-16` with `precision: day`
- `1857-12` with `precision: month`
- `mid nineteenth century` as an original expression with normalized interval only when justified
- `after sunset` as a relative expression linked to source context, not an invented clock time

## Spatial Precision

Spatial values should distinguish:

- exact coordinate from source or trusted gazetteer
- point approximation
- named place
- administrative area
- region
- route or linear feature
- uncertain area
- unknown or unstated

Coordinates derived from a named place must be marked as derived approximations. They are not equivalent to source-stated coordinates.

## Measurement Precision

Measurements, including intensity, magnitude, depth, distance, or damage estimates, should distinguish:

- source-stated value
- normalized value
- scale or unit
- range
- qualitative descriptor
- uncertainty note
- derivation method

## Validation Expectations

Validators should warn when:

- a normalized value has no source basis
- precision metadata is missing
- exact coordinates are provided for vague source locations
- exact dates are provided for vague source times
- uncertainty is only present in notes when structured precision fields are available

## Stage 0 Open Issue

The exact vocabulary should remain draft until the Stage 1 toy pack tests whether it can represent real examples without forcing false precision.
