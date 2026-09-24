
# DQM 21 extraneous nodes (Schema)

`ogc.dqm.schemas.extraneous_nodes` *v0.1*

number of faulty point-curve connections in the dataset

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## My Schema

Defines a set of properties that may be used in **any** JSON schema.

> Note these properties may be used in the "properties" sub-component of a GeoJSON object, as a simple object

The numeric properties "b" and "c" have an example SHACL rule that if c is present, then c > b
## Examples

### Examples
The content of this example. 
#### json
```json
{
      "extraneous_nodes": 2
}
```

#### jsonld
```jsonld
{
  "@context": "https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/extraneous_nodes/context.jsonld",
  "extraneous_nodes": 2
}
```

#### ttl
```ttl
@prefix dqm: <http://www.opengis.net/def/metamodel/isodqm/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

[] dqm:21 2 .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: DQM extraneous nodes
$defs:
  extraneous_nodes_value:
    type: number
properties:
  extraneous_nodes:
    $ref: '#/$defs/extraneous_nodes_value'
    x-jsonld-id: http://www.opengis.net/def/metamodel/isodqm/21
x-jsonld-prefixes:
  dqm: http://www.opengis.net/def/metamodel/isodqm/

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/extraneous_nodes/schema.json)
* JSON version: [schema.json](https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/extraneous_nodes/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "extraneous_nodes": "dqm:21",
    "dqm": "http://www.opengis.net/def/metamodel/isodqm/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/extraneous_nodes/context.jsonld)

## Sources

* [Sample source document](https://example.com/sources/1)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcsandpit/dqm-schemas](https://github.com/ogcsandpit/dqm-schemas)
* Path: `_sources/extraneous_nodes`

