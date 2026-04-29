---
title: DataBuilder - Scoped, Global
description: The DataBuilder API provides methods to create a series of data points for a metric. Use the sn\_clotho.Client.put\(\) method to save the values.Creates an instance of the DataBuilder class.Adds a series of data points to the DataBuilder object. Each data point is a time stamp and a value.Adds a data point to the DataBuilder object. Each data point is a time stamp and a value. This method does not save the data point in the metric. Use the sn\_clotho.Client.put\(\) method to save the values.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DataBuilder - Scoped, Global

The DataBuilder API provides methods to create a series of data points for a metric. Use the sn\_clotho.Client.put\(\) method to save the values.

You can call this class in scoped and global server scripts. When using the DataBuilder class, use the `sn_clotho` namespace identifier.

This class is part of the MetricBase application.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DataBuilder - DataBuilder\(Object glideRecord, String subject, String metric\)

Creates an instance of the DataBuilder class.

|Name|Type|Description|
|----|----|-----------|
|glideRecord|Object|GlideRecord from which to obtain the domain.|
|subject|String|The sys\_id of the GlideRecord associated with this series.|
|metric|String|The field name of the metric.|

The following example initializes a new instance of `DataBuilder` from the `sn_clotho` namespace using the `now_GR` parameter, which represents the current time or a specific time range, and the string parameter `'cpu_percentage'`, which is the name of the metric being tracked.

```
// Where cpu_percentage is the name of the metric
        var dataBuilder = new sn_clotho.DataBuilder(now_GR, 'cpu_percentage');
```

## DataBuilder - add\(GlideDateTime start, Array value\)

Adds a series of data points to the DataBuilder object. Each data point is a time stamp and a value.

Uses the start parameter and the retention policy collection period to calculate the time stamp for each value in the array. The first value has the start parameter as the time stamp. This method does not save the data in the MetricBase database. Use the sn\_clotho.Client.put\(\) method to save the values.

|Name|Type|Description|
|----|----|-----------|
|start|GlideDateTime|The time stamp for the first data point. Subsequent time stamps are calculated using the retention policy collection period.|
|value|Array|An array of numbers.|

|Type|Description|
|----|-----------|
|DataBuilder|The same DataBuilder object.|

The following example first initializes an array \(points\) containing three numerical values: 7, 0.5, and 273, which represent different data points related to CPU usage at a given timestamp. Then, the code initializes a new `sn_clotho.DataBuilder` object using `now_GR` \(a GlideRecord object\) represents the target database record where this data is being stored. `'cpu_percentage'` is the metric name used to track CPU usage.

A new time variable is created using GlideDateTime, which sets the object to the current date and time. Finally, the code uses `dataBuilder.add(time, points)` to store multiple data points in the Data Builder object.

```

var points = [7,0.5,273];
var dataBuilder = new sn_clotho.DataBuilder(now_GR, 'cpu_percentage');
// this creates a GlideDateTime object set to the current date and time
var time = new GlideDateTime();
dataBuilder.add(time, points);
```

## DataBuilder - add\(GlideDateTime start, Number value\)

Adds a data point to the DataBuilder object. Each data point is a time stamp and a value. This method does not save the data point in the metric. Use the sn\_clotho.Client.put\(\) method to save the values.

|Name|Type|Description|
|----|----|-----------|
|start|GlideDateTime|The time stamp for the data point.|
|value|Number|The value of the data point.|

|Type|Description|
|----|-----------|
|DataBuilder|The DataBuilder object.|

The following example first initializes a new instance of `DataBuilder` from the `sn_clotho` namespace using the parameters `now_GR` \(the target record\) and `'cpu_percentage'` \(the metric to track\). `GlideDateTime` initializes time to the current date and time. Finally, `dataBuilder.add()` stores the value `0.6` \(representing a value of 60% CPU usage\) at the current timestamp.

```
var dataBuilder = new sn_clotho.DataBuilder(now_GR, 'cpu_percentage');
// this creates a GlideDateTime object set to the current date and time
var time = new GlideDateTime();
dataBuilder.add(time, 0.6);
```

