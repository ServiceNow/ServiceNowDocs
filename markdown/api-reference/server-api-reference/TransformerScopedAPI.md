---
title: Transformer - Scoped, Global
description: The Transformer API manipulates time-series data to prepare the data for evaluation and analysis.Create a Transformer object.Run the transform.Specifies the field to use to group the data.Specify the metric field to be used in the transform.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Transformer - Scoped, Global

The Transformer API manipulates time-series data to prepare the data for evaluation and analysis.

You can call this API in scoped and global server scripts. When using the Transformer class, use the `sn_clotho` namespace identifier.

The general use case is to determine the period to be evaluated, select the records from the table with the metric field, define the type of transform to run, and then execute the transform.

```
// create the start and end time
       var start = new GlideDateTime();
	start.addSeconds(-1 * 60 * 60); 
	var end = new GlideDateTime();
	
	//mb_demo_drone is a table with metric fields. 
	var drones = new GlideRecord("mb_demo_drone");
	drones.addQuery("model", "Kingfisher Phantom");
	drones.query();

	//build a transform that returns a simple average
	var builder = new sn_clotho.Transformer(drones);
	builder.metric("mb_demo_mt_rem_battery").avg().label("Original");

	//execute transform and return result for visualization
	var result = builder.execute(start,end);
```

This class is part of the MetricBase application.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Transformer - Transformer\( GlideRecord sourceRecords\)

Create a Transformer object.

|Name|Type|Description|
|----|----|-----------|
|sourceRecords|GlideRecord|Contains the records for which metrics are to be evaluated. Can be one record or many.|

```
//where drones is a GlideRecord created from a table with a metric field
	var builder = new sn_clotho.Transformer(drones);

```

## Transformer - execute\(GlideDateTime start, GlideDateTime end\)

Run the transform.

Use the metric\(\) and groupBy\(\) methods before calling execute\(\). The execute\(\) method can only be called once for each Transformer object.

Actions performed as part of the transform do not change the data in the MetricBase database.

|Name|Type|Description|
|----|----|-----------|
|start|GlideDateTime|The beginning of the period to be evaluated.|
|end|GlideDateTime|The end of the period to be evaluated.|

|Type|Description|
|----|-----------|
|TransformResult|The transformed data.|

```
var minutesAgoStart = 60;
	var end = new GlideDateTime();
	var start = new GlideDateTime(end);
	start.addSeconds(-1 * 60 * minutesAgoStart);
	
	// query subject records
	var grDrone = new GlideRecord('mb_demo_drone');
	grDrone.query();
	
	// building transform; get the average transforms of a metric, grouping by model
	var transformer = new sn_clotho.Transformer(grDrone);
	transformer.groupBy("fleet").metric("mb_demo_mt_altitude").avg().label('avg - %g:fleet:');

	// execute and return result for visualization
	var tfrmResult = transformer.execute(start, end);
```

## Transformer - groupBy\(String field\)

Specifies the field to use to group the data.

If you are going to use the groupBy\(\) method, you must call it must before calling the execute\(\) method.

|Name|Type|Description|
|----|----|-----------|
|field|String|The field in the table to use to group the transform results.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that you can use to specify the transform characteristics.|

```
var transformer = new sn_clotho.Transformer(grDrone);
var trnsfrm = transformer.groupBy("fleet");
```

## Transformer - metric\(String metricName\)

Specify the metric field to be used in the transform.

You can specify multiple metrics to be used in the transform. The metric\(\) method cannot be called after theexecute\(\) method is called.

|Name|Type|Description|
|----|----|-----------|
|metricName|String|Name of the metric field.|

|Type|Description|
|----|-----------|
|TransformPart|A TransformPart object that can be used to specify the transform characteristics.|

```
var transformer = new sn_clotho.Transformer(grDrone);
var trnsfrm = transformer.metric("mb_demo_mt_altitude");
```

