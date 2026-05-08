---
title: Suppress schedule occurrences of your planned work
description: Streamline and optimize maintenance activities by suppressing duplicate planned work tasks when different schedules overlap.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Configure work plans, Planned Work Management, Set up work orders and tasks, Configure, Field Service Management]
---

# Suppress schedule occurrences of your planned work

Streamline and optimize maintenance activities by suppressing duplicate planned work tasks when different schedules overlap.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## About this task

Use schedule suppression to streamline tasks by removing duplicate tasks when schedules overlap. During the schedule suppression period, the system automatically cancels the identified duplicate scheduled tasks so they aren't executed as originally planned.

For example, consider an MRI machine with scheduled maintenance plans for both monthly and quarterly. If monthly maintenance occurs on the 15th and quarterly maintenance on the 22nd of every third month, these schedules overlap every three months. Both schedules might include tasks, such as air vents cleaning. To avoid doing the same task twice, a suppression period \(for example, seven days\) is used to check for overlaps. If the monthly tasks are covered in the quarterly schedule, the system suppresses the monthly maintenance. This helps prevent duplication, saves resources, and maintains operational efficiency.

**Note:**

-   To suppress schedules, the planned work schedules must be attached to similar work order templates or include similar tasks.
-   Work orders can be suppressed either fully or partially, depending on the attached work order templates and associated tasks.
-   If all work orders in the planned schedules match, they are fully suppressed and duplicate tasks are removed.
-   If work orders match partially, duplicate work orders for the matching tasks are removed, and work orders are created for the remaining tasks.

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open your work plan.

3.  In the **Planned Work Schedules** related list, select a schedule that you want to suppress with another schedule.

4.  In the **Schedule Suppressions** related list, select **New**.

5.  On the form, fill in the fields.

6.  <table id="table_h1v_gmt_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Suppress Period

</td><td>

Time period during which overlapping schedule occurrences are identified, allowing the system to suppress duplicate work order tasks.The property sn\_fsm\_planned\_wm.tolerance\_span allows you to customize the time window for the suppression period. For more information, see [Planned Work Management system properties](../reference/planned_work_management_sys_properties.md).

</td></tr><tr><td>

Active

</td><td>

Option to enable this suppression rule.

</td></tr><tr><td>

Suppress by

</td><td>

Name of the work schedule that you want to have priority over the current schedule.

</td></tr><tr><td>

Order

</td><td>

Order in which this suppression rule is evaluated.

</td></tr></tbody>
</table>7.  Select **Submit**.


## Result

The system changes the state of the schedule occurrence to suppressed and cancels the associated work order tasks.

