---
title: Client - Scoped, Global
description: The Client API provides methods to add data to the MetricBase database, to execute transforms on the MetricBase database, and to receive the results of the transforms.Create an instance of the client class to access the MetricBase database.Accumulates metric values at specified timestamp and saves the result to the database rather than overwriting the value.Remove a specified metric from a specified table in the MetricBase databaseRemove the data in the MetricBase database associated with the specified metric in the specified GlideRecord. Use this method for removing test data.Get all series from a specific dimension.Saves metric data to the MetricBase database.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Client- Scoped, Global

The Client API provides methods to add data to the MetricBase database, to execute transforms on the MetricBase database, and to receive the results of the transforms.

You can use the Client class in both scoped and global server scripts. This class is part of the MetricBase application and must run within the `sn_clotho` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Client - Client\(\)

Create an instance of the client class to access the MetricBase database.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var client = new sn_clotho.Client();
```

## Client - accumulate\(GlideRecord now\_GR, String metric\)

Accumulates metric values at specified timestamp and saves the result to the database rather than overwriting the value.

Use this method to handle metrics that can be summed for an accumulation, such as kilowatt-hours \(kWhs\) of electricity. Accumulate makes a call for each metric at the provided timestamp. For example, collected kilowatts for a heater, electric kettle, and washing machine would result in three calls to accumulate.

<table id="table_zsz_5jd_1db" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

now\_GR

</td><td>

GlideRecord

</td><td>

Name of the series GlideRecord from which to obtain the accumulated value.See also: [getSeries\(\)](ClientScopedAPI.md#)

</td></tr><tr><td>

default\_value

</td><td>

Number

</td><td>

Optional. Default value for accumulation at a given timestamp. Used only during the first call to accumulate if a value is unavailable for a given timestamp. A use case could be accumulating a watts metric for a total\_power. You want to accumulate watts for a router connected to an outlet without a power meter to measure it. If you know the consumption value and it is constant\), you can use the constant value as a default value to accumulate total\_power. For example, you would use 20 if the router is constantly plugged in and consumes 20 Watts.

 The timestamp value can be provided using the [DataBuilder](../../DataBuilderScoped/concept/DataBuilderScopedAPI.md#) API.

 Default: 0

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to accumulate the `total_power` metric value in a record called `building_a`.

```
var time = new GlideDateTime();

// total_power is the name of a metric within building_a which stores accumulated values

var dataBuilder1 = new sn_clotho.DataBuilder(building_a, "total_power");
// values to be accumulated
dataBuilder1.add(time, 3.5);
new sn_clotho.Client().accumulate(dataBuilder1, 0);

var dataBuilder2 = new sn_clotho.DataBuilder(building_a, "total_power");
// values to be accumulated
dataBuilder2.add(time, 3.5);
new sn_clotho.Client().accumulate(dataBuilder2, 0);

var dataBuilder3 = new sn_clotho.DataBuilder(building_a, "total_power");
// values to be accumulated
dataBuilder3.add(time, 3.5);
new sn_clotho.Client().accumulate(dataBuilder3, 0);

// As a result of these operations client will save value of
// 3.5+12+4.3+0(default value) at the timestamp 'time'
```

## Client - deleteMetric\(String tableName, String metricName\)

Remove a specified metric from a specified table in the MetricBase database

**Note:** This method deletes data from the MetricBase database. There is no recovery mechanism.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The name of the table whose specified metric is to be deleted.|
|metricName|String|The name of the metric.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to remove a metric from a table.

```
var client = new sn_clotho.Client();

// delete metric (Speed) from the Drones table
client.deleteMetric("mb_demo_drone", "mb_demo_mt_speed");
```

## Client - deleteSeries\(GlideRecord now\_GR, String metric\)

Remove the data in the MetricBase database associated with the specified metric in the specified GlideRecord. Use this method for removing test data.

**Note:** This method deletes data from the MetricBase database. There is no recovery mechanism.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|The records whose time series data for the specified metric is to be deleted.|
|metric|String|The name of the metric.|

|Type|Description|
|----|-----------|
|void| |

```
var client = new sn_clotho.Client();
//query drones of a specific model
var drones = new GlideRecord("mb_demo_drone");
drones.addQuery("model", "Kingfisher Phantom");
drones.query();

client.deleteSeries(drones, 'mb_demo_mt_speed');
```

## Client - getSeries\(GlideRecord now\_GR, String metricName, GlideDateTime lastUpdateBefore\)

Get all series from a specific dimension.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|The record from which to obtain the series.|
|metric|String|The name of the metric.|
|lastUpdateBefore|[GlideDateTime](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#)|Optional. Date in the future representing the end of the period to be evaluated.|

|Type|Description|
|----|-----------|
|Array|List of string sys\_ids representing the series containing data for the specified metric. If the **lastUpdateBefore** parameter is provided, returns series that have no data more recent than the lastUpdateBefore date \(non-inclusive\).|

The following example shows how to get the complete list of speed values listed in the Drones \[mb\_demo\_drone\] table.

```
var client = new sn_clotho.Client();

// query subject records
var grDrone = new GlideRecord('mb_demo_drone');
grDrone.query();

var series = client.getSeries(grDrone,'mb_demo_mt_speed');
```

## Client - put\(Object metricData\)

Saves metric data to the MetricBase database.

<table id="table_vxt_wvz_31b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

metricData

</td><td>

Object

</td><td>

One of the following:-   [DataBuilder](../../DataBuilderScoped/concept/DataBuilderScopedAPI.md#) object containing metric data.
-   Array of DataBuilder objects containing metric data.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var time = new GlideDateTime();
​
// two different GlideRecord instances and metrics
var dataBuilder = new sn_clotho.DataBuilder(now_GR, 'cpu_percentage');
dataBuilder.add(time, 0.6);
​
var dataBuilder2 = new sn_clotho.DataBuilder(gr2, 'disk_free_percentage');
dataBuilder2.add(time, 0.2);
​
new sn_clotho.Client().put([dataBuilder,dataBuilder2]);
```

