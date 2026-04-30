---
title: MetricInfo - Scoped, Global
description: The MetricInfo API provides methods to check if a metric is in the MetricBase database, and if so, to report its retention policy. Retention policies are reported in minutes.Creates an instance of the MetricInfo class.Gets the retention policy schedules of the specified metric.Indicates whether the specified metric is mapped to the table defined in a MetricInfo object.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MetricInfo - Scoped, Global

The MetricInfo API provides methods to check if a metric is in the MetricBase database, and if so, to report its retention policy. Retention policies are reported in minutes.

You can call this class in scoped and global server scripts. When using the MetricInfo class, use the `sn_clotho` namespace identifier.

This class is part of the [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) application.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MetricInfo – MetricInfo\(String table, String metric\)

Creates an instance of the MetricInfo class.

|Name|Type|Description|
|----|----|-----------|
|table|String|Metric table name listed in the Time Series Metrics \[sys\_metric\] table.|
|metric|String|Metric field name listed in the Time Series Metrics \[sys\_metric\] table. This field name must be mapped to the table name.|

The following example shows how to construct a MetricInfo object with the Altitude \(mb\_demo\_mt\_altitude\) metric associated with the Drones \[mb\_demo\_drone\] table.

```
var metricInfo =  new sn_clotho.MetricInfo('mb_demo_drone','mb_demo_mt_altitude');
```

## MetricInfo – getRetentionSchedulesInMinutes\(\)

Gets the retention policy schedules of the specified metric.

See also [MetricBase retention policies](https://www.servicenow.com/docs/access?context=metricbase-retention-policies&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rjl_vk3_fsb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON object containing key-value pairs that represent the retention policy schedules \(in minutes\) for the specified metric listed in the Retention Policies \[sys\_metric\_retention\_policy\] table.For each retention policy schedule belonging to the metric, the object contains a corresponding key-value pair that maps the retention duration to the sampling period.

-   Key – Retention duration of the retention policy schedule in minutes.

Data type: String

-   Value – Sampling period of the retention policy schedule in minutes.

Data type: Number


 ```
"<retentionDuration>": <samplingPeriod>
```

</td></tr></tbody>
</table>The following example shows how to loop over the retention policy schedules and compile a log message. The message contains the retention durations converted from minutes to days with their corresponding sampling periods.

```
// Function to convert minutes to days
function toDays(minutes) {
 return minutes / 60 / 24;
};

var metricInfo = new sn_clotho.MetricInfo('mb_demo_drone','mb_demo_mt_altitude');
var schedules = metricInfo.getRetentionSchedulesInMinutes();
var log = '';

// Compiles a log message with retention schedules
for (var duration in schedules) {
 log += "Retention duration is: " + toDays(duration) +
 " days, Sampling period is: " + schedules[duration] + " minutes\n";
}

gs.info(log);
```

Output:

```
Retention duration is: 8 days, Sampling period is: 1 minutes
Retention duration is: 94 days, Sampling period is: 10 minutes
Retention duration is: 397 days, Sampling period is: 60 minutes
```

## MetricInfo – isValid\(\)

Indicates whether the specified metric is mapped to the table defined in a MetricInfo object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_yqf_xk3_fsb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the metric specified in a MetricInfo object is mapped to the specified table.

 Valid values:

-   true: Specified metric is valid.
-   false: Specified metric or table either does not exist or the metric is not mapped to the table.

</td></tr></tbody>
</table>The following example shows how to check if the Altitude \(mb\_demo\_mt\_altitude\) metric is in the Drones \[mb\_demo\_drone\] table, and return its retention schedule if it is. The example output reflects the policy duration in minutes mapped to its interval sampling period.

```
var metricInfo =  new sn_clotho.MetricInfo('mb_demo_drone','mb_demo_mt_altitude');
if (metricInfo.isValid())
{
  var retentionSchedules = metricInfo.getRetentionSchedulesInMinutes();
  gs.info(JSON.stringify(retentionSchedules, null, 2));
}
else
{
  gs.info("metricInfo is invalid");
}
```

Output:

```
{
  "11520": 1,
  "135360": 10,
  "571680": 60
}
```

