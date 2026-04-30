---
title: Assign preferred agents to tasks
description: Identify the agents most preferred for working on a customer account and assign them to tasks.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Assign preferred agents to tasks

Identify the agents most preferred for working on a customer account and assign them to tasks.

## Before you begin

Role required: wm\_dispatcher, wm\_manager, wm\_admin

If you’re using Technician Preferences for dynamic scheduling, then you must have the **Prioritize preferred and secondary technicians** criterion added to your task filter to add preferred technicians. For more information, see [Example - configure dynamic scheduling to assign preferred technicians to tasks](excluded-preferred-agents.md).

If you're using Technician Preferences for Schedule Optimization then your administrator must [Configure the policy to assign preferred technicians to tasks](configure-the-policy-to-assign-preferred-technicians-to-tasks.md).

## About this task

The system copies account preferences from the 'wm\_agent\_assignment\_preferences' table to the 'wm\_task\_tech\_preference' table whenever the account field on a WOT is updated. If the task is already created and the account information is added later, the system also copies the data into the task preferences table from the account agent preferences if they are maintained.

Technician Preferences are used by dynamic scheduling, and Schedule Optimization. With dynamic scheduling, technician preferences are considered when you assign the task in Dispatcher Workspace, or when you auto-assign the task. With Schedule Optimization, the technician preferences are considered when the optimization engine auto-assigns tasks.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Order Tasks**.

2.  Select the work order task that you want to add a preferred agent to.

3.  Select the **Technician Preferences** tab.

4.  Select **New**.

5.  Add the agent details and set **Assignment Preference** to **Excluded Agent**.

    **Note:** Secondary indicates that the agent is the second option to assign a work order task to in case the preferred agent isn’t available.

6.  Select **Submit**.

7.  Select **Update**.


