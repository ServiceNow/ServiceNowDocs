---
title: Create a scheduling attribute for Schedule Optimization
description: Create scheduling attributes to specify which tasks to optimize and define the rules to perform the optimization. You can create different scheduling attributes configurations for each policy.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create a scheduling attribute for Schedule Optimization

Create scheduling attributes to specify which tasks to optimize and define the rules to perform the optimization. You can create different scheduling attributes configurations for each policy.

## Before you begin

Role required: wm\_admin

You must [Configure Schedule Optimization](../concept/schedule-optimization-engine.md).

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

        If your Task Filter references a custom field or a custom table, you must grant the sharedservice.worker user read access to those elements. For example, this applies if you use a table other than the default work order task table to submit work orders. For details, see [Schedule Optimization integration user access requirements](../reference/schedule-optimization-integration-user-access-requirements.md).

        The **Optimization Restricted** tab is displayed after the task filter record is created. This read-only field shows the conditions of work order tasks that are excluded from the optimization run.

7.  Enable dispatchers to run optimization for a group or territory from Dispatcher Workspace by adding a policy to the **On-demand applicable policies** related list.

    Dispatcher can manually trigger optimization to run for different policies at any time. For example, adding a policy that allows overtime will enable dispatchers to run optimization if agents are running behind schedule.

    1.  In the **On-demand applicable policies** related list, select **Edit**.

    2.  Add a policy.

    3.  Select **Submit**.

8.  Select **Update**.


## What to do next

[Create a batch for Schedule Optimization](create-an-optimization-batch.md#)

