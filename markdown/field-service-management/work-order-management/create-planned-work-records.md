---
title: Create planned work records
description: Create a list of planned work records based on the number of configured work schedules, matching records, or the number of templates mapped to the schedule.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure work plans, Planned Work Management, Set up work orders and tasks, Configure, Field Service Management]
---

# Create planned work records

Create a list of planned work records based on the number of configured work schedules, matching records, or the number of templates mapped to the schedule.

## Before you begin

You must assign a schedule to the work plan. For more information, see [Configure a work schedule](configure-work-plan.md).

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin and model\_manager

## About this task

The planned work records are used by the Planned Maintenance Nightly Run schedule job to create work orders. For more information, see [Run a scheduled job to execute a planned work schedule](run-schedule-job-planned-work.md).

Apply a work plan to the matching records and schedules to create planned work records. If multiple schedules are defined for a work plan, they all take effect on the matching records while creating planned work records. This same functionality exists for the work schedules that are used to apply the specific schedule to the matching records in the associated work plan.

You can also create planned work records through the Planned Work Management Workspace. Navigate to **All** &gt; **Planned Work Management** &gt; **Workspace**, and then select the List icon \(![List icon.](../image/ListIcon.png)\).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Planned Work Management** &gt; **Plans**.

2.  Create planned work records.

<table id="choicetable_nqq_y3j_35b"><thead><tr><th align="left" id="d75271e129">

To

</th><th align="left" id="d75271e132">

Do this

</th></tr></thead><tbody><tr><td id="d75271e138">

**Create planned work records for all the schedules defined for matching records**

</td><td>

1.  Open a desired plan from the list of work plans.
2.  In the related links section, select **Associate plan with filtered records**.


</td></tr><tr><td id="d75271e159">

**Create planned work records for an individual schedule defined for matching records**

</td><td>

1.  Open a desired plan from the list of work plans.
2.  In the Planned Work Schedules related list,select **New**.
3.  Open a desired schedule from the list of Planned Work Schedules.
4.  In the related links section, select **Associate schedule with filtered records**.


</td></tr></tbody>
</table>
## Result

The configured work schedule is applied to the matching records of that plan and generates a list of planned work records.

