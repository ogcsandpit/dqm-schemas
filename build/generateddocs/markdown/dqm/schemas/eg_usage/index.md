
# Example Feature with DQM (Schema)

`ogc.dqm.schemas.eg_usage` *v0.1*

Example of defining a feature with a specific DQM property

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## Feature with a DQM property

NB Records and STAC items are features and can be profiled with this model.


## Examples

### STAC item with link to provenance
Example GeoJSON feature with a DQM property

#### json
```json
{
  "id": "f1",
  "type": "Feature",
  "geometry": {
    "type": "LineString",
    "coordinates": [
      [
        -111.67183507997295,
        40.056709946862874
      ],
      [
        -111.71,
        40.156709946862874
      ]
    ]
  },
  "properties": {
    "extraneous_nodes": 3
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/eg_usage/context.jsonld",
  "id": "f1",
  "type": "Feature",
  "geometry": {
    "type": "LineString",
    "coordinates": [
      [
        -111.67183507997295,
        40.056709946862874
      ],
      [
        -111.71,
        40.156709946862875
      ]
    ]
  },
  "properties": {
    "extraneous_nodes": 3
  }
}
```

#### ttl
```ttl
@prefix dqm: <http://www.opengis.net/def/metamodel/isodqm/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://example.com/dqm/example1/f1> a geojson:Feature ;
    dqm:21 3 ;
    geojson:geometry [ a geojson:LineString ;
            geojson:coordinates ( ( -1.116718e+02 4.005671e+01 ) ( -1.1171e+02 4.015671e+01 ) ) ] .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Example of a sinmple GeoJSON Feature specialisation with a DQM measure
$defs:
  MyFeature:
    allOf:
    - $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/features/feature/schema.yaml
    - properties:
        properties:
          allOf:
          - $ref: https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/extraneous_nodes/schema.yaml
          - required:
            - extraneous_nodes
$ref: '#/$defs/MyFeature'

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/eg_usage/schema.json)
* JSON version: [schema.json](https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/eg_usage/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "features": {
      "@container": "@set",
      "@id": "geojson:features"
    },
    "type": "@type",
    "id": "@id",
    "properties": "@nest",
    "geometry": {
      "@context": {
        "coordinates": {
          "@container": "@list",
          "@id": "geojson:coordinates"
        }
      },
      "@id": "geojson:geometry"
    },
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "links": {
      "@context": {
        "href": {
          "@type": "@id",
          "@id": "oa:hasTarget"
        },
        "rel": {
          "@context": {
            "@base": "http://www.iana.org/assignments/relation/"
          },
          "@id": "http://www.iana.org/assignments/relation",
          "@type": "@id"
        },
        "type": "dct:type",
        "hreflang": "dct:language",
        "title": "rdfs:label",
        "length": "dct:extent"
      },
      "@id": "rdfs:seeAlso"
    },
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "dqm": "http://www.opengis.net/def/metamodel/isodqm/",
    "extraneous_nodes": "dqm:21",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcsandpit.github.io/dqm-schemas/build/annotated/dqm/schemas/eg_usage/context.jsonld)

## Sources

* [GeoDCAT Specification](http://www.opengis.net/def/metamodel/profiles/geodcat)
* [PROV-O Specification](https://www.w3.org/TR/prov-o/)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcsandpit/dqm-schemas](https://github.com/ogcsandpit/dqm-schemas)
* Path: `_sources/eg_usage`

