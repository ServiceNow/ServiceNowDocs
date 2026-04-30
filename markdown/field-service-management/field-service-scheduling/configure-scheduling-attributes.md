---
title: Create a scheduling attribute for Schedule Optimization
description: Create the scheduling attributes to specify which tasks to optimize and define the rules to perform the optimization.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create a scheduling attribute for Schedule Optimization

Create the scheduling attributes to specify which tasks to optimize and define the rules to perform the optimization.

## Before you begin

[Configuring Schedule Optimization](../concept/schedule-optimization-engine.md) must be setup.

Role required: wm\_admin

## About this task

This video demonstrates how to create a scheduling attribute for Schedule Optimization. 

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Scheduling Attributes**.

2.  Select **New**.

3.  On the form, fill in the fields.

    1.  Provide a name.

    2.  Select the default policy.

    3.  Select a travel estimate provider.

    4.  Select a travel estimate configuration.

        For more information, see [Setting up a travel estimate provider](setting-up-a-travel-estimate-provider.md).

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

