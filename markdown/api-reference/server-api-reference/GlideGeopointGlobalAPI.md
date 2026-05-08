---
title: GlideGeoPoint - Global
description: The GlideGeoPoint API enables you to get and set geopoint data type values in a table.Instantiates a GlideGeoPoint object. The GlideGeoPoint object adds semantic awareness to longitude and latitude values that are otherwise stored as strings.Instantiates the GlideGeoPoint object according to provided longitude and latitude values.Copies longitude and latitude points values to instantiate a new GlideGeoPoint object.Returns the geopoint of the current user in a user-friendly format.Returns a list of geo point coordinate values for a given field name of type geo point.Returns the latitude value of the GlideGeoPoint object.Returns the longitude value of the GlideGeoPoint object.Returns a string containing the programmatic longitude and latitude value of the current GlideGeoPoint object.Sets the longitude and latitude values of the geopoint.Sets the longitude and latitude values of the geopoint using a single comma-delimited value.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideGeoPoint- Global

The GlideGeoPoint API enables you to get and set geopoint data type values in a table.

This API is available by default. The geopoint data type allows you to store a latitude and longitude values in a single field within a table. Using the GlideGeoPoint API, you can instantiate new GlideGeoPoint objects, create new geopoints for a specific table, or retrieve single latitude, longitude or geotype values. For additional information on how to implement specific use cases like inserting new records using a geopoint, computing distances between geopoint locations, or querying for nearby geopoint locations, see [GlideGeoPoint Developer Guide](../../../../../integrate/guides/GlideGeoPoint/concept/geopoint-dev-guide.md#).

Key aspects of the geotype data type are:

-   It consists of a pair of decimal numbers representing longitude and latitude values.
-   The range for longitude is \(-180, 180\]. Any value outside this range is normalized to the equivalent value inside this range.
-   The range for latitude is \[-90, 90\]. Any value outside this range is normalized to the equivalent value inside this range.
-   Geopoint values are always accepted as input and display as a comma-separated pair: “longitude,latitude”. Parentheses may optionally surround the expression.
-   Both longitude and latitude values are stored up to 6 decimal places of precision.

**Note:** GlideGeoPoint API values are always listed in longitude, latitude order.

The examples on this page assume that a custom table is pre-populated with fields containing the geopoint field type. For more information about this data type, see Geo point field type and Function field.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideGeoPoint - GlideGeoPoint\(\)

Instantiates a GlideGeoPoint object. The GlideGeoPoint object adds semantic awareness to longitude and latitude values that are otherwise stored as strings.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to initialize a new GlideGeoPoint object as a null value.

```
var gp = new GlideGeoPoint();
```

## GlideGeoPoint - GlideGeoPoint\(String longitude, String latitude\)

Instantiates the GlideGeoPoint object according to provided longitude and latitude values.

|Name|Type|Description|
|----|----|-----------|
|longitude|String|The longitude coordinate of the geopoint.|
|latitude|String|The latitude coordinate of the geopoint.|

|Type|Description|
|----|-----------|
|geopoint|The resultant GlideGeoPoint object.|

The following example shows how providing longitude and latitude values initializes the object accordingly.

```
// Providing longitude and latitude values initializes the object accordingly 
var gp = new GlideGeoPoint(10.123, 25.987);  
gs.info("geopoint: " + gp);
```

Output:

```
geopoint: 10.123000,25.987000
```

## GlideGeoPoint - GlideGeoPoint\(Object geoPoint\)

Copies longitude and latitude points values to instantiate a new GlideGeoPoint object.

|Name|Type|Description|
|----|----|-----------|
|geoPoint|Object|The geopoint instance that you want copy.|

|Type|Description|
|----|-----------|
|geopoint|The resultant GlideGeoPoint object.|

The following example shows how to copy longitude and latitude values to instantiate a new GlideGeoPoint object.

```
var gp = new GlideGeoPoint(135, -64);
var gpCopy = new GlideGeoPoint(gp); 
gs.info("geopoint: " + gpCopy);
```

Output:

```
geopoint: 135,-64
```

## GlideGeoPoint - getDisplayValue\(\)

Returns the geopoint of the current user in a user-friendly format.

The getDisplayValue\(\) method returns a single geopoint value. For information about how to retrieve all geopoint values from a specific table, see [GlideGeoPoint Developer Guide](../../../../../integrate/guides/GlideGeoPoint/concept/geopoint-dev-guide.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The value of the longitude and latitude coordinates set in the object.|

```
var gp = new GlideGeoPoint(); 
gp.setValue(76.25, 49.75);      
gs.info("geopoint: " + gp); 
gs.info("getDisplayValue(): " + gp.getDisplayValue());
```

Output:

```
geopoint: 76.250000,49.750000 
getDisplayValue(): (76.250000, 49.750000)
```

## GlideGeoPoint - getGeoPoint\(String geo\_point\_field\_name\)

Returns a list of geo point coordinate values for a given field name of type geo point.

<table id="table_bz4_jsl_5bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

geo\_point\_field\_name

</td><td>

String

</td><td>

Name of the geo point field.**Note:** You can also locate field names under dictionary elements defined on a table to see associated fields of geo point type.

Table: Dictionary Entry \[sys\_dictionary\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Resultant GlideGeoPoint object.|

In the following example, 'test\_table' is a table which contains the 'geo\_point' field of geo point type. The test\_table has one record populated in the geo\_point column with a value of \(-30.560000,-54.330000\). The example code returns the latitude and longitude coordinates and display value of the record in geo\_point column.

```
var gr_Test = new GlideRecord('test_table');
gr_Test.query();
gr_Test.next();
var gp = gr_Test.getGeoPoint('geo_point');
gs.info("getLatitude(): " + gp.getLatitude());
gs.info("getLongitude(): " + gp.getLongitude());
gs.info("getDisplayValue(): " + gp.getDisplayValue());
```

Output:

```
getLatitude(): -54.33
getLongitude(): -30.560000000000002 
getDisplayValue(): (-30.560000, -54.330000)
```

## GlideGeoPoint - getLatitude\(\)

Returns the latitude value of the GlideGeoPoint object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The latitude value of the GlideGeoPoint object.|

```
var gp = new GlideGeoPoint(); 
gp.setValue(76.25, 49.75);      

gs.info("geopoint: " + gp); 
gs.info("getLatitude(): " + gp.getLatitude());
```

Output:

```
geopoint: 76.250000,49.750000 
getLatitude(): 49.75
```

## GlideGeoPoint - getLongitude\(\)

Returns the longitude value of the GlideGeoPoint object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The longitude value of the GlideGeoPoint object.|

```
var gp = new GlideGeoPoint(); 
gp.setValue(76.25, 49.75);      
gs.info("geopoint: " + gp);  
gs.info("getLongitude(): " + gp.getLongitude());
```

Output:

```
geopoint: 76.250000,49.750000 
 getLongitude(): 76.25
```

## GlideGeoPoint - getValue\(\)

Returns a string containing the programmatic longitude and latitude value of the current GlideGeoPoint object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The longitude and latitude value of the current GlideGeoPoint object.|

```
 var gp = new GlideGeoPoint(); 
gp.setValue(76.25, 49.75);      
gs.info("geopoint: " + gp);
gs.info("getValue(): " + gp.getValue());
```

Output:

```
geopoint: 76.250000,49.750000
getValue(): 76.250000,49.750000
```

## GlideGeoPoint - setValue\(String longitude, String latitude\)

Sets the longitude and latitude values of the geopoint.

|Name|Type|Description|
|----|----|-----------|
|longitude|String|The longitudinal coordinate of the geopoint.|
|latitude|String|The latitude coordinate of the geopoint.|

|Type|Description|
|----|-----------|
|String|The longitude and latitude value set on the GlideGeoPoint object.|

```
var gp = new GlideGeoPoint(); 
gp.setValue("-28.48,38.91");      
gs.info("geopoint: " + gp);
```

Output:

```
geopoint: -28.480000,38.910000
```

## GlideGeoPoint - setValue\(String value\)

Sets the longitude and latitude values of the geopoint using a single comma-delimited value.

|Name|Type|Description|
|----|----|-----------|
|value|String|A comma-delimited value containing longitude and latitude points respectively.|

|Type|Description|
|----|-----------|
|String|The longitude and latitude value set on the GlideGeoPoint object.|

The following example shows how to set the longitude and latitude values using a single string.

```
var gp = new GlideGeoPoint();
gp.setValue(23.4, 56.7);
```

Output:

```
geopoint: -23.400000,56.700000
```

