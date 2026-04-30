---
title: Create scripted allocation metrics - Legacy
description: You can create scripted metrics and methods using the standard Cost Allocation Metric form.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Allocation metrics - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create scripted allocation metrics - Legacy

You can create scripted metrics and methods using the standard Cost Allocation Metric form.

## Before you begin

Role required: cost\_transparency\_admin

## About this task

You can create weighted metrics in scripted form and scripted methods [Allocation metrics - Legacy](../concept/c_AllocationMetrics.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Consumption Metrics** &gt; **Create Scripted Weighted Metric**.

2.  Click **New**.

3.  Select **Scripted weighted metric** or **Scripted method** in the **Type** field.

4.  Fill out the fields on the form as appropriate \(see table\).

5.  Click **Submit**.

    ![The Cost Allocation Metric form](../image/scripted_metric_geneva.png "Example scripted metric")

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive name of the metric.|
    |Allocation group|The group associated with this metric. On the Cost Allocation Method form, the selection of the group limits the selection of the metric to only those metrics that use the group.|
    |System metric|If this metric was created by the application in the workbench.|
    |Type|The type of script. Select **Scripted method** or **Scripted weighted metric** to make the **Script** field appear.|
    |Script|The script to calculate the allocation.|

    |Field|Description|
    |-----|-----------|
    |Cost Allocation Methods|Methods that use the metric. You can add methods to the related list or navigate to the method form and select the metric you just created.|

    **Note:** You cannot delete a rule that is referenced by a locked allocation line.


**Parent Topic:**[Allocation metrics - Legacy](../concept/c_AllocationMetrics.md)

