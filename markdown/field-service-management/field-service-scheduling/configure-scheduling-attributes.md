---
title: Create a scheduling attribute for Schedule Optimization
description: Create the scheduling attributes to specify which tasks to optimize and define the rules to perform the optimization.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create a scheduling attribute for Schedule Optimization

Create the scheduling attributes to specify which tasks to optimize and define the rules to perform the optimization.

## Before you begin

Role required: wm\_admin

[Configuring Schedule Optimization](../concept/schedule-optimization-engine.md) must be set up.

## About this task

This video demonstrates how to create a scheduling attribute for Schedule Optimization. 

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Scheduling Attributes**.

2.  Select **New**.

3.  On the form, fill in the fields.

    1.  Provide a name.

    2.  Select the default policy.

    3.  Select a primary travel estimate configuration.

    4.  Select a secondary travel estimate provider.

        If you do not set up a secondary travel estimate provider and your primary configuration is unavailable, optimization will use the default straight-line configuration. For more information, see [Setting up a travel estimate provider](setting-up-a-travel-estimate-provider.md).

4.  Select **Submit**.

5.  Select the record you just created.

6.  In the **Work Type Task Filters** tab, select **New** to choose the task conditions to be considered when optimization runs.

    1.  Provide a name for the task filter.

    2.  Select or create a **Work configuration**.

    3.  Use the **Optimization Targets** tab add one or more filter condition.

    4.  Select **Submit**.

        **Note:** The **Optimization Restricted** tab will be displayed after the task filter record is created. This read-only field shows the conditions of work order tasks that are excluded from the optimization run.

7.  Enable dispatchers to run optimization for a group or territory from Dispatcher Workspace by adding a policy to the **On-demand applicable policies** related list.

    **Note:** Dispatcher can manually trigger optimization to run for different policies at any time. For example, adding a policy that allows overtime will enable dispatchers to run optimization if agents are running behind schedule.

    1.  In the **On-demand applicable policies** related list, select **Edit**.

    2.  Add a policy.

    3.  Select **Submit**.

8.  Select **Update**.


## What to do next

[Create a batch for Schedule Optimization](create-an-optimization-batch.md#)

