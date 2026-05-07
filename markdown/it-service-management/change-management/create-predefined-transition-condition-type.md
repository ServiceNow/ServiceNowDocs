---
title: Create predefined transition condition types
description: Create predefined transition conditions to reuse the conditions for your change models.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# Create predefined transition condition types

Create predefined transition conditions to reuse the conditions for your change models.

## Before you begin

Role required: change\_manager

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Module** &gt; **Change Model Condition Types**.

2.  On the Change Model Condition Types page, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the condition type. This name is displayed in the **Requires** field on the Model State Transition Condition form.|
    |Description|Detailed description of the condition type.|
    |Condition Type|Type of condition. The available options are condition or script.|
    |Table name|Table name that the condition is based on.|
    |Condition \(Condition builder\)|Conditions that must be fulfilled for processing the transition.|
    |Condition \(Script\)|Script that must be fulfilled for processing the transition. If passed, it returns a value of true. This field is available only if script is selected from **Condition Type**.|

4.  Click **Submit**.


**Parent Topic:**[Create a Change model](create-a-change-model.md)

