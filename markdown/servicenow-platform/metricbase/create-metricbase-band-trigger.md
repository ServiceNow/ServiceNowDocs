---
title: Create a MetricBase band trigger
description: Create a MetricBase band trigger that detects when a metric value falls within a range of values.
locale: en-US
release: zurich
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Trigger flows, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a MetricBase band trigger

Create a MetricBase band trigger that detects when a metric value falls within a range of values.

## Before you begin

Role required: admin

## About this task

Band triggers execute when metrics fall outside of or within a range of values.

![Band trigger solutions](../image/band-trigger-values.png "Band trigger values")

## Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **MetricBase Triggers** &gt; **Trigger Definitions**.

2.  Select **New**.

3.  On the **MetricBase** Trigger Creation form, select the **Band Trigger** option.

4.  On the form, fill in the fields.

    The trigger levels are not initially visible on this form. You configure the levels later.

<table id="table_khd_cjn_pbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the band trigger.

</td></tr><tr><td>

Table name

</td><td>

Table in the MetricBase database that contains the metric that you want to monitor. The only tables that appear when you click the search icon are the tables that you specified in the time-series metrics.

 If you select a metric before you select a table, only tables that have that metric appear in the **Table name** dialog box.

</td></tr><tr><td>

Metric

</td><td>

Table metric that you want to monitor that is specified by the **Table name**. The only metrics that appear when you click the search icon are the metrics in that table.

 If you select a metric before you specify a **Table name**, the metrics in all your time-series metrics appear. After you select a metric, only the tables that contain that metric appear when you click the search icon that is next to the **Table name**.

</td></tr><tr><td>

Active

</td><td>

Option to activate the trigger.

</td></tr><tr><td>

Description

</td><td>

Description of the trigger.

</td></tr><tr><td>

Aggregator

</td><td>

Aggregation value that you select: **None**, **Max**, **Min**, or **Average**. **None** means that you use the last value in the collection period.

</td></tr><tr><td>

Window

</td><td>

Length of time used to calculate the aggregation function. For example, assume the **Window** is 1 hour and the aggregator is **Min**, and a new data point is added to the series. The system calculates the new minimum using the new data window \(the last hour of data including the new data point\). The new minimum is compared to the different trigger levels to determine whether to execute the trigger.

</td></tr></tbody>
</table>5.  Select **Save**.

    A new record is created.

6.  In the MetricBase Band Trigger Levels section on the record you just created, double-click each cell to add values that specify trigger parameters.

    |Field|Description|
    |-----|-----------|
    |Level|Numbers that indicate increasing severity. For example, you might define the altitude for level 1 to be less than 50 meters, but above 25 meters, and the altitude for level 2 to be less than or equal to 25. Each level should trigger a different flow. **Level** is often used in Condition Scripts. See [Execute triggers conditionally](create-action-condition.md).|
    |Function|Function that makes the **Value** the maximum or minimum of the lower end of the band. Therefore, the function defines whether trigger values are inside or outside of the band. For example, if the **Function** is **Less than**, the trigger executes when the metric goes below the band value.|
    |Value|Lower end of the band. See the following image.|
    |Band Function|Function that makes the **Band Value** the maximum or minimum value of the upper end of the band. Therefore, the band function defines whether trigger values are inside or outside of the band. For example, if the **Band Function** is **Greater than**, the trigger executes when the metric goes above the band value. See the following image.|
    |Band Value|Upper end of the band. See the following image.|
    |Tolerance|Sets tolerance margins around the **Value** and **Band Value** to prevent repeatedly executing a trigger for small fluctuations in the data. After a trigger executes, the data must exceed the tolerance to execute the trigger again. See the following image.|

    ![Band trigger overview](../image/band-trigger-overview.png)

    For example, assume the **Function** is **Greater than**, the **Value** is 25, and the **Band Value** is 50.

    -   If the **Tolerance** is 0, the trigger executes for all values that are less than 50 and greater than 25.
    -   If the **Tolerance** is 5, the ranges are 50 ± 5 \(45-55\) and 25 ± 5 \(20-30\).
    -   If the last two data points in order were 51 and 49, the trigger executes because 49 is below the **Band Value**.
    -   If the next two data points in order are 51 and 49, the trigger doesn't execute again because the values are within the tolerance range since the last trigger execution.
7.  Add one or more rows to the table to create multi-layered triggering behavior.

    **Note:** You must define at least two levels in a band trigger so that there are levels to transition between.

    Typically, each additional row \(level\) indicates a more severe condition. The Workflow Studio flow associated with the level should warn with increasing severity.

8.  Select **Update**.

9.  Add a triggering condition that determines whether a trigger executes a Workflow Studio flow.

    See [Execute triggers conditionally](create-action-condition.md).


## Band Trigger form

![Band trigger form](../image/band-trigger-form.png)

## What to do next

Associate this trigger with a Workflow Studio flow. For more information, see [Assign a trigger to a flow](assign-trigger-to-workflow.md).

