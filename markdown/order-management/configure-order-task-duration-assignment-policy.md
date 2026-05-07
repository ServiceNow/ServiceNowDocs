---
title: Configure the Order Task Duration Assignment Policy
description: Configure the Order Task Duration Assignment Policy using Workflow Studio. This policy determines how long each task should take to complete, when it should start, and when it's expected to finish, enabling accurate scheduling, resource planning, and timeline visibility across the order life cycle.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Jeopardy Management, Order management, Configure, Sales Customer Relationship Management]
---

# Configure the Order Task Duration Assignment Policy

Configure the Order Task Duration Assignment Policy using Workflow Studio. This policy determines how long each task should take to complete, when it should start, and when it's expected to finish, enabling accurate scheduling, resource planning, and timeline visibility across the order life cycle.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Order Task Duration Assignment Policy**.

    ![The image shows the Order Task Duration Assignment policy window in Workflow Studio.](../image/jm-order-task-duration-assignment.png)

3.  On the Order Task Duration Assignment Policy decision table, fill in the fields.

<table id="table_wfc_vbj_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request type

</td><td>

Order task for which you want to add a duration time.

</td></tr><tr><td>

Order task account

</td><td>

Order task account associated with the task.

</td></tr><tr><td>

Duration

</td><td>

Allotted time for this task. For example, 2 Days 6 Hours.**Note:** The allotted time for order tasks must be the same as the allotted time in the SLA definition assigned to the order task.

</td></tr></tbody>
</table>4.  Select **Save**.


## What to do next

The next step is to configure SLA definitions for Jeopardy Management. For more information, see [create-sla-definitions.md](create-sla-definitions.md).

