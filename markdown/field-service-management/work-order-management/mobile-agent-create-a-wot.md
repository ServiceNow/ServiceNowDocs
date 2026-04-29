---
title: Create a task on ServiceNow Agent
description: As an agent, create work order tasks using the ServiceNow Agent application.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Create a task on ServiceNow Agent

As an agent, create work order tasks using the ServiceNow Agent application.

## Before you begin

Role required: wm\_agent

To add locations, agents must have the sn\_fsm\_service\_loc.wm\_service\_location\_write role.

## Procedure

1.  Navigate to the Create new work form.

    -   To create a work order task from Draft tasks, navigate to **My Work** &gt; **Draft tasks** &gt; **Create new work**.
    -   To create a work order task from an asset, navigate to the asset then tap **Create new work**.
    -   To create a work order task from the Work order overflow menu, navigate to the work order and select the **Overflow menu** ![Overflow icon.](../image/more-actions-mobile-icon.png). Select **Create new work**.
    -   To create a sibling work order task, open the selected work order task. Then navigate to **Related** &gt; **Sibling work order tasks** &gt; **Create new sibling task**.
    -   To create a work order task from an Install base Affected Product, navigate to the install base affected product then tap **Create new work**.
2.  Fill in the fields.

<table id="table_hsq_4tg_mr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work order

</td><td>

Work order this task is assigned to.

</td></tr><tr><td>

Company

</td><td>

Company for which the work order was opened.

</td></tr><tr><td>

Asset

</td><td>

Parts required to execute the task.**Note:** If selected, Install base item and Location fields are hidden.

</td></tr><tr><td>

Install base item

</td><td>

The install base item that user has issue with.**Note:** If selected, Asset and Location fields are hidden.

</td></tr><tr><td>

Location

</td><td>

Geographical area where the work needs to be done. The location is critical for determining the agent assigned to the task.If you don’t want to use the auto-populated location, you can add an ad hoc location. For more information, see [Setting ad-hoc locations in work orders and work order tasks](../concept/service-locations-work-orders.md).

</td></tr><tr><td>

Priority

</td><td>

Priority of this task.

</td></tr><tr><td>

Short Description

</td><td>

Brief explanation of the task.

</td></tr><tr><td>

Description

</td><td>

Exact technical description of the work to be performed. Provide as much detail about the problem as possible to avoid extra communication with the customer in later stages of the work order life cycle.

</td></tr></tbody>
</table>3.  Tap **Submit**.


