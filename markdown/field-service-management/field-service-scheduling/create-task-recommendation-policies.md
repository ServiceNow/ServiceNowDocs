---
title: Create Task Recommendation Policies
description: Create policies to recommend the best available work order tasks for agents based on the specified rules and conditions.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Intelligent Task Recommendations, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create Task Recommendation Policies

Create policies to recommend the best available work order tasks for agents based on the specified rules and conditions.

## Before you begin

Role required: admin, wm\_admin

## About this task

You can use the default `Standard task recommendation` policy or create a new policy. The following steps explain how you can create a policy.

## Procedure

1.  Navigate to **Field Service** &gt; **Task Recommendation Administration** &gt; **Task Recommendation Policies**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Display Name|Display name of the task recommendation policy.|
    |Name|Name of the task recommendation policy stored in the wm\_task table.|
    |Table|Task table that is selected for the recommendation policy.|
    |Applicable to|Applications that are supported for the policy.|
    |Application module|Application module under which the policy exists.|
    |Application|Application that contains this record.|
    |Active|Option to indicate whether the policy is available for consideration when recommending work order tasks.|

4.  In the **Query condition** field, add filter conditions to recommend tasks.

    1.  To recommend the best matched tasks that are in the Pending Dispatch state to an agent, click **Add Filter Condition** and create the condition.

        For example, **\[State\] \[is\] \[Pending Dispatch\] AND \[Active\] \[is\] \[true\]**.

    2.  To apply an alternate condition set to the query, click **Add "Or" Clause** and add conditions for the second set.

5.  Click **Submit**.


## Result

The recommendation policy is created successfully. The policy has the Filtering Constraints and Ranking Criteria related lists.

## What to do next

You can customize optional filter constraints and ranking criteria. For more information, see [Create a filter constraint or a ranking criteria for a task recommendation policy](create-filtering-constraint.md).

