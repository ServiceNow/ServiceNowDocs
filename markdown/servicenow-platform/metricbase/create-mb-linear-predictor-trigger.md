---
title: Create a MetricBase linear predictor trigger
description: Create a MetricBase linear predictor trigger to detect when a metric is likely to cross a specified threshold within a specified period of time.
locale: en-US
release: yokohama
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Trigger flows, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a MetricBase linear predictor trigger

Create a MetricBase linear predictor trigger to detect when a metric is likely to cross a specified threshold within a specified period of time.

## Before you begin

Role required: admin

## About this task

The linear predictor trigger uses past data to generate a line that predicts future values. When MetricBase predicts that the linear value reaches a threshold, the trigger executes.

![Linear predictor crosses the threshold.](../image/linear-predictor-trigger.png "Linear predictor crosses the threshold")

If the most recent data point reaches the threshold, the trigger executes regardless of the linear prediction.

Trigger parameters include how much past data to use in the calculation of the prediction, how far ahead to look, and the level of confidence that you accept.

## Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **MetricBase Triggers** &gt; **Trigger Definitions**.

2.  Select **New**.

3.  On the **MetricBase** Trigger Creation form, select the **Linear Predictor Trigger** option.

4.  On the form, fill in the fields.

    The trigger levels are not initially visible on this form. You configure the levels later.

<table id="table_khd_cjn_pbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the linear predictor trigger.

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

</td></tr><tr><td id="window-mb-cell-calc-line">

Window

</td><td>

Length of time used to calculate the line that predicts the future course of the value. For example, you might want to use the last 10 minutes of data to calculate the linear predictor. If the value is too long, the line does not reflect current trends. If the value is too short, the line might follow the raw values too closely and not accurately reflect the overall trend of the values. The value must be at least 10 times the sampling period that is defined by the sampling rate of your **Metric**. **Warning:** Do not confuse this value with the **Window** value in the [trigger level](create-mb-linear-predictor-trigger.md#window-mb-trigger-level). That value specifies how far into the future that you want the linear predictor to look to see if the **Metric** is likely to cross the **Threshold**.

</td></tr><tr><td>

Confidence Level \(%\)

</td><td>

A measure of how closely the real data fits the linear prediction of the data. A confidence level of 95% means that the real value must be within 5% of the predicted value to execute a trigger. If you only want to trigger when the real values are close to the predicted values, choose a high confidence percentage. If you are willing to accept real data that varies more significantly from the predicted values as being valid, select a lower confidence level, for example, 80%.

</td></tr><tr><td>

Trend

</td><td>

Direction of the trend: upward or downward. For example, the value is increasing or decreasing toward the **Threshold**.

</td></tr><tr><td>

Threshold

</td><td>

Target value that the metric is expected to reach before the trigger executes.

</td></tr><tr><td>

Description

</td><td>

Description of the trigger.

</td></tr></tbody>
</table>5.  Select **Save**.

    A new record is created.

6.  In the MetricBase Linear Predictor Trigger Levels section on the record you just created, double-click each cell to add values that specify trigger parameters.

<table id="table_khd_cjn_pbba"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Level

</td><td>

Numbers that indicate increasing severity. Each level should trigger a different flow. For example, you might define the following:-   **Level 1**

Battery is predicted to reach 20% in 30 minutes.

-   **Level 2**

Battery is predicted to reach 20% in 5 minutes.

 **Level** is often used in Condition Scripts. See [Execute triggers conditionally](create-action-condition.md).

</td></tr><tr><td>

Function

</td><td>

Comparative function to use on the threshold value. **Less than or is** is the only available option. For example, battery life **Less than or is** 30 minutes.

</td></tr><tr><td id="window-mb-trigger-level">

Window

</td><td>

How far into the future that you want the linear predictor to look to see if the metric is predicted to cross the threshold. **Warning:** Do not confuse this value with the **Window** value in the [trigger definition form](create-mb-linear-predictor-trigger.md#window-mb-cell-calc-line). That value specifies how much data to use \(measured in time\) to calculate the slope of the predictor line.

</td></tr></tbody>
</table>7.  Add rows to the table to create multi-layered triggering behavior.

    Typically, each additional row \(level\) indicates a more severe condition. The Workflow Studio flow associated with the level should warn with increasing severity.

8.  Select **Update**.

9.  Add a triggering condition that determines whether a trigger executes a Workflow Studio flow.

    See [Execute triggers conditionally](create-action-condition.md).


## Linear Predictor form

![Linear predictor form](../image/linear-predictor-form.png)

## What to do next

Associate this trigger with a Workflow Studio flow. For more information, see [Assign a trigger to a flow](assign-trigger-to-workflow.md).

