---
title: Review a task
description: As a reviewer, review the details of a work order task. If the details are sufficient, you can close the task. If more information is required, send the task back to the agent so they can add the requested details.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Review a task

As a reviewer, review the details of a work order task. If the details are sufficient, you can close the task. If more information is required, send the task back to the agent so they can add the requested details.

## Before you begin

Role required: sn\_fsm\_quality.wm\_quality\_agent

Ensure that the Field Service Quality Management plugin is active. For more information, see [Activate Field Service Quality Management](activate-quality-mgmt.md).

## About this task

When an agent closes a task, the task will be sent to you for review. You can close the task if the details are sufficient, or you can send the task back to the agent requesting more details.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Reviewing** &gt; **Quality reviews**.

2.  Select a work order task.

3.  Choose one of the following:

    -   If the task details are sufficient, select **Close task**.
    -   If more information is required, add what information is needed from the agent in the **Work notes** field. Then, select **Send back to agent**.

## Result

If the task details are sufficient, the task is closed.

If more information was required, the task is sent back to the agent and the substate is set to Needs information. The agent will receive a notification that the selected work order task needs more information. In the Mobile Agent® application, the agent can update the work order task with the requested details and send the task back to the reviewer. For more information, see [Respond to a reviewed task](../concept/close-wo-wot-mobile.md#).

