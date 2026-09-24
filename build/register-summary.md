# Data Quality Measures Schemas

Implementation models (JSON/YAML schemas, but potentially XML and RDF)


Data Quality Measures may require complex (non-scalar) value objects, in which case canonical schemas for these values are required to achieve interoperability.


## Building Blocks

### `ogc.dqm.schemas.extraneous_nodes` — DQM 21 extraneous nodes

**Type:** schema

number of faulty point-curve connections in the dataset

### `ogc.dqm.schemas.measure` — Measure

**Type:** schema

Utility datatype for a Measure, a numerical value with a units of measure. The QUDT namespaces is defined by default, but may be overridden by a well formed URI or CURIE pattern.

### `ogc.dqm.schemas.eg_usage` — Example Feature with DQM

**Type:** schema

Example of defining a feature with a specific DQM property

