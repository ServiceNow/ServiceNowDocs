---
title: Close a work order task as incomplete
description: Close a work order task as incomplete if there is work pending on the task.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Execute work order tasks, Updating task status in web interface, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Close a work order task as incomplete

Close a work order task as incomplete if there is work pending on the task.

## Before you begin

Role required: wm\_agent

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Agent** &gt; **Assigned to me**.

2.  Open a work order task.

3.  Click **Close Incomplete**.

    The **Close Incomplete** pop-up appears.

4.  Do one of the following.

    |Option|Description|
    |------|-----------|
    |**Clone the task and create a follow-on task**|From the **Create a follow on task?** list, select **Yes**.|
    |**Close the work order as incomplete without creating a follow-on task**|From the **Create a follow on task?** list, select **No**.|

5.  In the **Reason for the incomplete closure** field, enter a reason for not completing the task.

    This information is copied to the **Work Notes** field on the work order task form.

6.  Click **OK**.

    The status of all unused parts automatically changes to **In-Stock**.

    The parent work order state changes based on the following conditions:

<table id="table_v5b_4jy_jgb"><thead><tr><th align="center">

If

</th><th align="center">

The work order state changes to

</th></tr></thead><tbody><tr><td>

All work order tasks are in the **Closed-Complete** or **Canceled** state and at least one work order task is in **Closed-Incomplete** state.

</td><td>

**Closed - Incomplete**

</td></tr><tr><td>

Only one work order task is associated with a work order and that task generates a follow-on task, which is in **Draft** state.

</td><td>

**Awaiting Qualification**

</td></tr><tr><td>

More than one work order task is associated with a work order and one or more those tasks generate a follow-on task, which is in **Draft** state.

</td><td>

**Work in Progress**

</td></tr><tr><td>

All follow-on tasks generated from any of the work order tasks are in **Closed Complete** state. **Note:** The task that generated the follow-on task will be in **Closed Incomplete** state.

</td><td>

**Closed Complete**

</td></tr></tbody>
</table>    **Note:** Additionally,

    Closing child Work Order task also closes parent work order.

    This business rule is configured on parent \(sm\_task\) table and runs when a \(sm\_task\) record's state changes. There is logic hardcoded to rollup the state change to its parent.

    If this behavior is not desired for work orders you can implement the following condition on this business rule to ensure this business rule does not run for \(wm\_task/wm\_order\) records.

    Condition = current.sys\_class\_name != 'wm\_task' &amp;&amp; current.sys\_class\_name != 'wm\_order'.


**Parent Topic:**[Execute work order tasks](../concept/c_ExecuteWorkOrderTasks.md)

