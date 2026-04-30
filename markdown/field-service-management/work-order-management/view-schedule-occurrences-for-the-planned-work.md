---
title: View schedule occurrences for a planned work
description: A Schedule occurrence represents a single instance when a work order is expected to be created. Schedule occurrences are automatically created when a schedule is created or updated.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-02-02"
reading_time_minutes: 3
breadcrumb: [Manage a work order for the planned work, Manage work orders, Prepare work orders, Use, Field Service Management]
---

# View schedule occurrences for a planned work

A Schedule occurrence represents a single instance when a work order is expected to be created. Schedule occurrences are automatically created when a schedule is created or updated.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

You must have configured a work schedule and attached a template to it. For more information see, [Configure a work schedule](configure-work-plan.md).

## About this task

A schedule occurrence in Planned Work Management is a particular event within a repeating maintenance schedule. Each schedule occurrence is an automatically created record, representing one planned maintenance event as part of an ongoing schedule. It serves as a link between the maintenance plan and the work order that will be carried out. Schedule occurrences also helps in auditing the previous work orders for the maintenance plan.

For duration-based schedules \(**Trigger** in the work schedule is **Duration**\), the schedule occurrences are created immediately when a work schedule is configured.

For meter-based schedules \(**Trigger** in the work schedule is **Duration**\), the schedule occurrences are created only when the meter threshold is reached.

Schedule occurrences are numbered sequentially based on the creation order. Upon configuring the schedule, schedule occurrences with **Pending** state are created for the next immediate maintenance work required. Once the work orders for these schedule occurrences are created, the state is updated to **Scheduled** and new schedule occurrences for the next maintenance is generated.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open a plan from the list of work plans.

3.  In the **Planned Work Schedules** related list, select the schedule for which you want to view the associated schedule occurrences.

4.  Select **Schedule Occurrences** related list.

    The fields of a schedule occurrence are described in the below mentioned table.

<table id="table_msw_lfz_d3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the schedule occurrence.

</td></tr><tr><td>

Active

</td><td>

Indicates if the schedule occurrence is active. If the value is **true**, the schedule occurrence is active.

</td></tr><tr><td>

Asset

</td><td>

Reference to the asset record if the maintenance is for an asset \(source is an asset\).

</td></tr><tr><td>

CI

</td><td>

Reference to the CI record of the maintenance is for a configuration item \(source is a CI\).

</td></tr><tr><td>

Document table

</td><td>

Table name of the source record \(for example, alm\_asset, cmdb\_ci\).

</td></tr><tr><td>

Earliest start date

</td><td>

Earliest date on which the maintenance can begin for this schedule occurrence.

</td></tr><tr><td>

Inactivated on

</td><td>

Time-stamp when the schedule occurrence was deactivated.

</td></tr><tr><td>

Last completion date

</td><td>

Date of completion of the previous work order for this schedule.

</td></tr><tr><td>

Last completion value

</td><td>

Meter or duration value when the last maintenance was completed.

</td></tr><tr><td>

Planned work record

</td><td>

Reference to the planned work record that generated this schedule occurrence.

</td></tr><tr><td>

Requested due by

</td><td>

Due date by when the maintenance should be completed.

</td></tr><tr><td>

State

</td><td>

The current state of the schedule occurrence. The available states are:-   Pending: Work order for the schedule occurrence is not yet generated
-   Scheduled: Work order for the schedule occurrence has been generated
-   Partially suppressed: Some tasks are suppressed and some associated work orders are cancelled
-   Fully suppressed: All the tasks are suppressed and no work orders are generated
-   Completed: Work order for the schedule occurrence is complete
-   Canceled: The work order for the schedule occurrence is cancelled


</td></tr><tr><td>

Work notes

</td><td>

Journal to track updates, changes, and notes about the schedule occurrence.

</td></tr><tr><td>

Source ID

</td><td>

Sys\_id of the source record to which the occurrence applies.

</td></tr><tr><td>

User

</td><td>

Refer to the user record when the schedule applies to a user.

</td></tr><tr><td>

Inactivated on

</td><td>

Time-stamp when the schedule occurrence was deactivated.

</td></tr><tr><td>

Last completion date

</td><td>

Date when the previous work order for the schedule occurrence was completed.

</td></tr><tr><td>

Last completion value

</td><td>

The date on which the previous work order for this schedule was completed.

</td></tr><tr><td>

Task generated

</td><td>

Indicates whether work order tasks for the schedule occurrence have been created

</td></tr><tr><td>

Suppressed by

</td><td>

List of other schedules that suppresses this schedule occurrence.

</td></tr></tbody>
</table>    **Note:** Admins can configure the fields to be displayed.


