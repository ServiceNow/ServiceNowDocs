---
title: Create a MetricBase gap trigger
description: Create a MetricBase gap trigger to alert you when MetricBase stops receiving data.
locale: en-US
release: yokohama
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Trigger flows, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a MetricBase gap trigger

Create a MetricBase gap trigger to alert you when MetricBase stops receiving data.

## Before you begin

Role required: admin

## About this task

Gap triggers execute when MetricBase stops receiving data for a specified period.

![Gap trigger executes on missing data in the database](../image/mb-gap-trigger.png "Gap trigger executes on missing data")

You can define multiple trigger levels to indicate different severities. For example, you can set a gap of 10 minutes as level 1, a gap of 20 minutes as level 2, and so on. Each level should trigger a different Workflow Studio flow. The difference between gap durations on different levels must be at least 10 minutes. For example, if you set level 1 to a gap of 10 minutes, you must set level 2 to a gap of 20 minutes or more.

**Note:** If you make the gap durations between levels less than 10 minutes, MetricBase displays an error message and deletes the level that you added.

Polling frequency is calculated using the difference between gap durations on different levels and dividing by 2 \(rounded down\). For example, given the following:

-   Level 1 triggers after 5 minutes of missing data
-   Level 2 triggers after 30 minutes of missing data

The polling frequency is 12 minutes, because Floor\(\(30-5\)/2\) = 12 minutes.

The maximum polling frequency is every 5 minutes, and the minimum frequency is every 30 minutes. If a trigger has only one level, the polling frequency is 30 minutes.

MetricBase searches through the data that is stored in the MetricBase database, not through incoming data. Therefore, a gap trigger might execute after the gap when data is missing. For example, if MetricBase polls every 10 minutes and the gap is 30 minutes of missing data, the trigger might execute as late as 40 minutes after the data was last received.

## Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **Workflow Studio** &gt; **Trigger Definitions**.

2.  Select **New**.

3.  On the **MetricBase** Trigger Creation form, select the **Gap Trigger** option.

4.  On the form, fill in the fields.

    The trigger levels are not initially visible on this form. You configure the levels later.

<table id="table_khd_cjn_pbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the trigger.

</td></tr><tr><td>

Table name

</td><td>

Table in the MetricBase database that contains the metric that you want to monitor. The only tables that appear when you click the search icon are the tables that you specified in the time-series metrics.

 If you select a metric before you select a table, only tables that have that metric appear in the **Table name** dialog box.

</td></tr><tr><td>

Active

</td><td>

Option to activate the trigger.

</td></tr><tr><td>

Metric

</td><td>

Table metric that you want to monitor that is specified by the **Table name**. The only metrics that appear when you click the search icon are the metrics in that table.

 If you select a metric before you specify a **Table name**, the metrics in all your time-series metrics appear. After you select a metric, only the tables that contain that metric appear when you click the search icon that is next to the **Table name**.

</td></tr><tr><td>

Description

</td><td>

Description of the trigger.

</td></tr></tbody>
</table>5.  Select **Save**.

    A new record is created.

6.  In the MetricBase Gap Trigger Levels area on the record you just created, double-click each cell to add values that specify trigger parameters.

    |Field|Description|
    |-----|-----------|
    |Level|Numbers that indicate increasing severity. For example, you might define level 1 to be no data for 10 minutes. Level 2 might be no data for 20 minutes. Each level should trigger a different flow. **Level** is often used in Condition Scripts. See [Execute triggers conditionally](create-action-condition.md).|
    |Function|Function, **Greater than or is**, which means that this trigger executes when the gap in received data is greater than the value that you specify in the **Window** field. There is only one option for the function, and it cannot be left empty or MetricBase displays an error message.|
    |Window|Length of time that no data has been received that executes the trigger. The format is hours:minutes:seconds. For example, 00:20:00 means that this trigger executes after 20 minutes of missing data.|

7.  Add rows to the table to create multi-layered triggering behavior.

    Typically, each additional row \(level\) indicates a more severe condition. The Workflow Studio flow associated with the level should warn with increasing severity.

8.  Select **Update**.

9.  Add a triggering condition that determines whether a trigger executes a Workflow Studio flow.

    See [Execute triggers conditionally](create-action-condition.md).


## Gap Trigger form

![Gap Trigger form](../image/gap-trigger-form.png)

## What to do next

Associate this trigger with a Workflow Studio flow. For more information, see [Assign a trigger to a flow](assign-trigger-to-workflow.md).

