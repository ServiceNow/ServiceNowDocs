---
title: Data - Scoped, Global
description: The Data API provides a data object that contains the results of transform performed by a sn\_clotho.Client.transform\(\) method.Returns the end time for data in the Data object.Returns the label assigned by the sn\_clotho.ClothoTransform.label\(\) method.Returns the name of the metric of the data series. Returns null when the data object is associated with multiple data series.Returns the time period in milliseconds.Returns the start time for data in the Data object.Returns the subject of the data series. Returns null when the data object is associated with multiple data series.Returns the name of the table assigned in the DataSelector class constructor. Returns null when the data object is associated with multiple data series.Returns an array of values.Returns the number of values in the Data object.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Data - Scoped, Global

The Data API provides a data object that contains the results of transform performed by a sn\_clotho.Client.transform\(\) method.

Do not use a constructor to create an instance of this class, instead use the object returned by the sn\_clotho.Client.transform\(\) method.

You can call this class in scoped and global server scripts. This class runs in the `sn_clotho` namespace identifier.

This class is part of the MetricBase application.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped Data - getEnd\(\)

Returns the end time for data in the Data object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideDateTime|The end of the time period.|

## Scoped Data - getLabel\(\)

Returns the label assigned by the sn\_clotho.ClothoTransform.label\(\) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The label assigned to the data.|

## Scoped Data - getMetricName\(\)

Returns the name of the metric of the data series. Returns null when the data object is associated with multiple data series.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the metric field. Returns null when the data object is associated with multiple data series.|

## Scoped Data - getPeriod\(\)

Returns the time period in milliseconds.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The elapsed time in seconds.|

## Scoped Data - getStart\(\)

Returns the start time for data in the Data object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideDateTime|The time for the first data point.|

## Scoped Data - getSubject\(\)

Returns the subject of the data series. Returns null when the data object is associated with multiple data series.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The subject field value of the subject GlideRecord. This is generally the sys\_id of the subject GlideRecord.|

## Scoped Data - getTableName\(\)

Returns the name of the table assigned in the DataSelector class constructor. Returns null when the data object is associated with multiple data series.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Table name. Returns null when the data object is associated with multiple data series.|

## Scoped Data - getValues\(\)

Returns an array of values.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of numbers.|

## Scoped Data - size\(\)

Returns the number of values in the Data object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of values in the object.|

