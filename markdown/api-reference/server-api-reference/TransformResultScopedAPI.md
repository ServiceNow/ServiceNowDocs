---
title: TransformResult - Scoped, Global
description: The TransformResult API provides methods that return the result of a transformation run on time-series data.Returns an array of Data objects. Returns an error if no group was specified for the transform.Returns the transformed data with the specified label.Returns a single Data object, or null if the result is empty.Returns the transformed data as an array. This method turns a Data object into an array.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TransformResult - Scoped, Global

The TransformResult API provides methods that return the result of a transformation run on time-series data.

You can use this API in both scoped and global server scripts. When using the Transformer class in a scoped application, use the `sn_clotho` namespace identifier.

There is no constructor for this class. TransformResult objects are returned by many TransformPart methods.

This class is part of the MetricBase application.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TransformResult - byGroup\(\)

Returns an array of Data objects. Returns an error if no group was specified for the transform.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of Data objects, with each object corresponding to a group.|

## TransformResult - getByLabel\(String label\)

Returns the transformed data with the specified label.

|Name|Type|Description|
|----|----|-----------|
|label|String|The label that identifies the data to be retrieved.|

|Type|Description|
|----|-----------|
|Data|The Data object with the transform results.|

## TransformResult - getData\(\)

Returns a single Data object, or null if the result is empty.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Data|The Data object with the transform results.|

## TransformResult - toArray\(\)

Returns the transformed data as an array. This method turns a Data object into an array.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|The Data object formatted as an array.|

