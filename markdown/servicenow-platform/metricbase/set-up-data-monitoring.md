---
title: Create a time-series definition in MetricBase
description: Specify the metric that you want to store, how often to collect it, and how long to store it in MetricBase.
locale: en-US
release: australia
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Define and collect data, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a time-series definition in MetricBase

Specify the metric that you want to store, how often to collect it, and how long to store it in MetricBase.

## Before you begin

-   [Install MetricBase](request-metricbase.md)
-   Role required: clotho\_admin

## Procedure

1.  Navigate to **MetricBase** &gt; **Time Series Metrics**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ayv_rrh_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Intuitive name for the **Metric field name**. For example, altitude could be the label for the metric field name, mb-altitude.

</td></tr><tr><td>

Table name

</td><td>

Name of the table to add the metric to in the MetricBase database. For example, in the MetricBase Demo, the mb\_drone table stores the drone data. Each column in the table is a different metric, for example, altitude, length, and speed.

</td></tr><tr><td>

Metric field name

</td><td>

Name of the time-series metric that records. For example, mb-altitude. You can think of it as the name of a column in the MetricBase database table.

</td></tr><tr><td>

Retention policy

</td><td>

Sampling frequency and how long MetricBase keeps the values in the database. You cannot customize the value. For a definition of the values, click the magnifying glass and then a policy. The coarser the sampling rate, the less data that stores. Use the coarsest sampling rate that works for your dataset. For example, do not collect data every minute if collecting it once an hour suffices. See [MetricBase retention policies](../reference/metricbase-retention-policies.md) for a description of the policies you can select.

</td></tr><tr><td>

Retention policy aggregator

</td><td>

Operator that aggregates the data in a sampling period. For example, last, minimum, maximum, and average.

</td></tr><tr><td>

Display value aggregator

</td><td>

The aggregation method in use when using `<table-name>.list` where &lt;table-name&gt; is a table in the MetricBase database. This value is unrelated to the retention policy. For a definition of the options, see [MetricBase transforms](https://www.servicenow.com/docs/access?context=metricbase-transforms&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Display value aggregate duration

</td><td>

Duration that is used to calculate the aggregation only when using the list view. For example, `<table-name>.list` where &lt;table-name&gt; is a table in the MetricBase database. This value is unrelated to the retention policy.

</td></tr><tr><td>

Subject field

</td><td>

You can select a unique table column as your subject for the metric. The unique column must be designated on the table before you select it. For example, if your metric tracks temperatures in different houses, you can make the house address column the subject of your metric. The house address column on your table must be unique before you set the subject field.**Note:** The sys\_id column is the default unique column.

</td></tr><tr><td>

Data Type

</td><td>

You can specify the data type of the subject field.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

You've created a time-series specification for a metric that you want to track.

## What to do next

Sample the data according to the time-series specification and send it from an instance to the MetricBase database server.

Use the REST or JavaScript APIs to send the data to the MetricBase database at the rate that is prescribed by the time-series definition. See [Developer resources](../concept/developer-resources.md).

**Important:** Send the data at the rate that the time-series definition prescribes. If you send the data at a different rate or for a different duration, you receive an error. Make sure to aggregate the data according to the time-series metric definition. Also, the MetricBase database only stores values of data type float.

