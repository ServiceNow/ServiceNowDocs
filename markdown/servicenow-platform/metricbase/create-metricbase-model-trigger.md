---
title: Create a MetricBase model trigger
description: Model triggers execute when the time-series data deviates from expected values.
locale: en-US
release: zurich
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Trigger flows, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a MetricBase model trigger

Model triggers execute when the time-series data deviates from expected values.

## Before you begin

Role required: admin

## About this task

There are four model types supported: autoregressive integrated moving average \(ARIMA\), probabilistic exponentially weighted moving average \(PEWMA\), Holt-Winters, and seasonal trend decomposition using Loess \(STL\).  MetricBase  uses the model to create a definition of expected, normal values.

## Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **MetricBase Triggers** &gt; **Trigger Definitions**.

2.  Select **New**.

3.  On the **MetricBase** Trigger Creation form, select the **Model Trigger** option.

4.  On the form, fill in the fields.

    The trigger levels are not initially visible on this form. You configure the levels later.

<table id="table_khd_cjn_pbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name the model trigger.

</td></tr><tr><td>

Model

</td><td>

Trained model this trigger uses. See [Create and train a predictive model](train-a-model.md).

</td></tr><tr><td>

Metric

</td><td>

Table metric that you want to monitor. This value is set automatically based on the model, which means you cannot set it yourself.

</td></tr><tr><td>

Table name

</td><td>

Table in the  MetricBase  database that contains the metric that you want to monitor. This value is set automatically based on the model, which means you cannot set it yourself.

</td></tr><tr><td>

Active

</td><td>

Option to activate the trigger.

</td></tr><tr><td>

Description

</td><td>

Description of the trigger.

</td></tr><tr><td>

Spike Direction

</td><td>

Specify whether you want to trigger only on anomalies that occur above predicted values \(upward\), below predicted values \(downward\), or both \(either\).

</td></tr></tbody>
</table>5.  Select **Save**.

    A new record is created.

6.  In the MetricBase Model Trigger Levels area on the record you just created, double-click each cell to add values that specify trigger parameters.

    |Column|Description|
    |------|-----------|
    |Level|Numbers that indicate increasing severity. For example, you might define level 1 to be 2 standard deviations from the mean. Level 2 might be 4 standard deviations. Each level should trigger a different Workflow Studio flow. **Level** is often used in Condition Scripts. See [Execute triggers conditionally](create-action-condition.md).|
    |Function|Always **Greater than or is**, meaning that in order to trigger, the time-series metric must be greater than or equal to the number of standard deviations from the mean specified in **Number of Standard Deviations**.|
    |Number of Standard Deviation|Float value specifying the number of standard deviations the time-series metric must be away from the mean to trigger an alert at this level.|

7.  Add rows to the table to create multi-layered triggering behavior.

    Typically, each additional row \(level\) indicates a more severe condition. The Workflow Studio flow associated with the level should warn with increasing severity.

8.  Select **Update**.

9.  Add a triggering condition that determines whether a trigger executes a Workflow Studio flow.

    See [Execute triggers conditionally](create-action-condition.md).

10. Test your model and trigger on real data before deploying to production.


## Model Trigger form

![Model Trigger form](../image/model-trigger-form.png)

## What to do next

Associate this trigger with a Workflow Studio flow. For more information, see [Assign a trigger to a flow](assign-trigger-to-workflow.md).

