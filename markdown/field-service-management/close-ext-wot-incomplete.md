---
title: Close an external work order task as incomplete
description: Close a work order task as incomplete if there is work pending on the task.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Work order tasks on the Field Service Contractor Portal, Field Service Contractor Portal, Using Field Service Management, Field Service Management]
---

# Close an external work order task as incomplete

Close a work order task as incomplete if there is work pending on the task.

## Before you begin

Role required: wm\_ext\_agent and wm\_ext\_manager

## Procedure

1.  Navigate to **All** &gt; **Field Service Contractor Portal** &gt; **Homepage**.

2.  Open a work order task that is already in progress.

3.  Click **Close Incomplete**.

4.  Close or create a follow-on task.

    |To|Do this|
    |---|-------|
    |**Create a new follow-on task**|From the **Create a follow on task?** list, select **Yes**.|
    |**Close the work order as incomplete without creating a follow-on task.**|From the **Create a follow on task?** list, select **No**.|

5.  In the **Reason for the incomplete closure** field, enter a reason for not completing the task.

    This information is copied to the Work Notes field on the work order task form.

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


## Result

The task is closed successfully and a follow-up task is created if you have selected **Yes** from the Create a follow-on task? list.

**Parent Topic:**[Work order tasks on the Field Service Contractor Portal](../concept/work-order-tasks.md)

