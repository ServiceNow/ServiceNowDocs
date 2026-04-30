---
title: Activity conditions
description: Create the exit conditions for your activity in the Condition column and set the order for each..
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activity conditions

Create the exit conditions for your activity in the **Condition** column and set the order for each..

The system evaluates the condition with the lowest order number first and stops when it finds the first true condition. The system delays evaluation of conditions with an **Else** value set to **true** until all conditions with an **Else** value set to **false** are evaluated. If the system does not find a true condition, it looks for a default condition in which the value for **Else** is **true** and takes this exit. You must have at least one default exit condition, or the activity hangs when the workflow runs.

The following are possible conditions you might create for an activity:

|Condition|Evaluation|
|---------|----------|
|Success|Tests for a success condition. **Else** is set to **false** and the **Order** is set to **100**. If this condition is true, the activity takes the **Success** exit. If this condition is false, the system evaluates the next condition in order.|
|Retry|Tests for a condition that runs the activity again. **Else** is set to **false**. If this condition is true, the activity runs again. If this condition is false, the system takes the default **Failure** exit.|
|Failure|Default condition that allows the workflow to continue if the other conditions in the activity are false. **Else** is set to **true**.|

![Sample activity conditions](../image/CustomActivityConditions.png)

**Parent Topic:**[Create custom activities using custom activity designer templates](../task/create-custom-activities.md)

