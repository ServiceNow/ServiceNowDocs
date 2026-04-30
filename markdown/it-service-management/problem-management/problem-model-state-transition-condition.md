---
title: Problem Management model state transition condition form
description: Description of the field values for the model state transition condition form.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Problem Management model state transition condition form

Description of the field values for the model state transition condition form.

|Field|Description|
|-----|-----------|
|Name|Unique name for the condition.|
|State Transition|State that you're applying the transition condition to. This field is automatically set with the state that you're applying the condition to.|
|Description|Detailed description of the condition.|
|Requires|Condition for your transition. You can select a pre-defined condition or select **Transition Condition** to define a condition. To create pre-defined conditions, see [Create predefined conditions](../../change-management/task/create-predefined-transition-condition-type.md).|
|Condition \(condition builder\)|Condition on the problem task record that must be fulfilled to enable the transition.|
|Condition \(script\)|Script that must be fulfilled to enable the transition. The script returns a value of **True** when passed.|
|Active|Option to make the condition active.|

**Parent Topic:**[Reference section for Problem Management](../concept/reference-section-for-problem-management.md)

