---
title: Create Service Level Agreement definitions in Jeopardy Management
description: Create and link Service Level Agreements \(SLAs\) to tasks in a fulfillment workflow as part of configuring Jeopardy Management. SLAs are assigned to tasks and define the amount of time a task should take. After SLAs are linked to a task, the SLA monitors the task and the fulfillment process.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 3
breadcrumb: [Configuring Jeopardy Management, Order management, Configure, Sales Customer Relationship Management]
---

# Create Service Level Agreement definitions in Jeopardy Management

Create and link Service Level Agreements \(SLAs\) to tasks in a fulfillment workflow as part of configuring Jeopardy Management. SLAs are assigned to tasks and define the amount of time a task should take. After SLAs are linked to a task, the SLA monitors the task and the fulfillment process.

## Before you begin

You must be in the Order Management application scope.

Role required: admin

## About this task

Creating SLA definitions are a part of configuring Jeopardy Management. SLAs are linked to tasks in a fulfillment plan. The SLA tracks of the time that a task takes to complete. If the task takes longer than the SLA definition, jeopardy alerts are created. Fulfillment managers can monitor the jeopardy levels and be alerted when tasks are falling into jeopardy. Defining SLAs involves the following steps:

-   Define SLA for an order task​.
-   Set the expected duration for the task​.
-   Define when to start, stop, and pause the SLA clock.

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **SLA** &gt; **SLA Definitions**.

2.  Select **New**.

3.  On the SLA Definition form, fill in the fields.

<table id="table_fzg_nxf_qs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that identifies the SLA definition.

</td></tr><tr><td>

Type

</td><td>

This must be set to SLA.

</td></tr><tr><td>

Target

</td><td>

This must be set to Resolution.

</td></tr><tr><td>

Table

</td><td>

This must be set to **Order Task \(sn\_ind\_tmt\_ord\_order\_task\)**.

</td></tr><tr><td>

Flow

</td><td>

This must be set to **SLA processing flow for Order Task** flow or a previously-created custom flow that is extended from the base system version to perform the jeopardy calculations.

</td></tr><tr><td>

Enable logging

</td><td>

Activates debug logging. The debug logging information includes details of the conditions that have matched or not matched. The information also provides the before and the after values for the task SLA and task records.

</td></tr><tr><td>

Duration type

</td><td>

This must be set to **User specified duration**.

</td></tr><tr><td>

Duration

</td><td>

Task duration time. The duration time must match the time set in the **Order Task Duration Assignment Policy**.

</td></tr><tr><td>

Schedule source

</td><td>

This must be set to **SLA definition**.

</td></tr><tr><td>

Schedule

</td><td>

This must be set to **24 x 7**.

</td></tr><tr><td>

Timezone Source

</td><td>

This must be set to **The SLA definition's timezone**.

</td></tr><tr><td class="sub-head" colspan="2">

Tabs

</td></tr><tr><td>

Start condition

</td><td>

Define the starting conditions in which the SLA parameters are started.

</td></tr><tr><td>

Pause condition

</td><td>

Define the conditions under which the SLA suspends the elapsed time.**Note:** The Start and Suspend conditions in the SLA definition must match the same conditions in the Order Task Duration Assignment Policy. For more information, see [Configure the Order Task Duration Assignment Policy](configure-order-task-duration-assignment-policy.md).

</td></tr><tr><td>

Stop condition

</td><td>

Define the conditions under which the SLA is completed. If all these conditions match, then the task SLA is completed regardless of whether it's breached.

</td></tr><tr><td>

Reset condition

</td><td>

Determines whether the existing task is canceled or completed on task SLA reset. Defines the conditions under which the running SLA is canceled or completed and a new SLA is attached. For a new SLA to be attached, the start condition must match.Reset condition also helps to configure SLAs when the value of any field on the task record changes, changes to, or changes from a value.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Configure the decision tables. For more information, see [Configure the Order Line Jeopardy Level Calculation Policy](configure-order-line-jeopardy-level-calculation-policy.md).

