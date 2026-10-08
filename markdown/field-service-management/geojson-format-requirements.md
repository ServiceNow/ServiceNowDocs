---
title: GeoJSON format requirements for territory geographies
description: GeoJSON format requirements define the structure, geometry types, and coordinate rules that territory geographies must follow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/field-service-management/geojson-format-requirements.html
release: australia
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Reference, Field Service Management]
---

# GeoJSON format requirements for territory geographies

GeoJSON format requirements define the structure, geometry types, and coordinate rules that territory geographies must follow.

## Geography types

The **Geography Type** field on the Territory Geography \[sn\_tp\_territory\_geography\] table determines how the system uses GeoJSON.

|Value|Label|Behavior|
|-----|-----|--------|
|`geojson`|GeoJSON|You provide the GeoJSON directly. This is the default geography type.|
|`composite`|Composite Geography|The system generates the GeoJSON automatically by merging multiple referenced geographies into a single MultiPolygon. Before merging, the system approximates each circle as a 64-point polygon.|
|`matching_attributes`|Matching Attributes|The territory uses ZIP code, city, state, or country attributes for matching instead of GeoJSON. The system skips GeoJSON validation for this geography type.|

When you select **GeoJSON** in the **Geography Type** field, make sure that the content of the **GeoJSON** field meets the requirements. This applies whether you import a GeoJSON file or paste the GeoJSON directly.

## Required top-level structure

GeoJSON must be wrapped in a FeatureCollection at the top level.

```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": { ... },
      "properties": { }
    }
  ]
}
```

-   Set `type` to `FeatureCollection`. This value is case-sensitive.
-   Include at least one Feature object in the `features` array.
-   Give each Feature a `type` of `Feature`, a `geometry` object, and a `properties` object.

## Supported geometry types

Territory geographies support the Polygon, MultiPolygon, and Point \(circle\) geometry types.

<table id="table_supported_geometry_types"><thead><tr><th>

Geometry type

</th><th>

Description

</th><th>

Structure

</th></tr></thead><tbody><tr><td>

Polygon

</td><td>

A single closed polygon shape.

</td><td>

```json
{
  "type": "Polygon",
  "coordinates": [
    [ [lng, lat], [lng, lat], [lng, lat], [lng, lat] ]
  ]
}
```

</td></tr><tr><td>

MultiPolygon

</td><td>

Multiple separate polygon regions.

</td><td>

```json
{
  "type": "MultiPolygon",
  "coordinates": [
    [ [ [lng, lat], [lng, lat], [lng, lat], [lng, lat] ] ],
    [ [ [lng, lat], [lng, lat], [lng, lat], [lng, lat] ] ]
  ]
}
```

</td></tr><tr><td>

Point \(circle\)

</td><td>

A center point with a radius in meters, which represents a circle. Add the `radius` property to the `properties` object. The radius must be a number in meters.

</td><td>

```json
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [lng, lat]
  },
  "properties": { "radius": 5000 }
}
```

</td></tr></tbody>
</table>## Unsupported GeoJSON types

Territory geographies accept only the Polygon, MultiPolygon, and Point \(circle\) geometry types. The following standard GeoJSON geometry types aren't recognized:

-   LineString
-   MultiLineString
-   MultiPoint
-   GeometryCollection

## Coordinate rules

-   Enter each coordinate as `[longitude, latitude]`, with exactly two numeric values.
-   Use a longitude value from -180 through 180.
-   Use a latitude value from -90 through 90.
-   Include at least four coordinate pairs in each linear ring of a Polygon or MultiPolygon.
-   Close each ring by making the first and last coordinates identical.

## Multi-feature constraints

-   A FeatureCollection can contain multiple Polygon and MultiPolygon features.
-   A FeatureCollection can contain only one Point \(circle\) feature.
-   A FeatureCollection can contain either a circle or polygons, not both.

**Parent Topic:**[Field Service Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/fsm-reference.md)

