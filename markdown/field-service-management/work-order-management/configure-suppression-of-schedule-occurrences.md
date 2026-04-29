---
title: Configure schedule occurrence suppression
description: Streamline and optimize maintenance activities by suppressing duplicate planned work tasks when different schedules overlap.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Planned Work Management, Set up work orders and tasks, Configure, Field Service Management]
---

# Configure schedule occurrence suppression

Streamline and optimize maintenance activities by suppressing duplicate planned work tasks when different schedules overlap.

Use schedule suppression to streamline tasks by removing duplicate tasks when schedules overlap. During the schedule suppression period, the system automatically cancels the identified duplicate scheduled tasks so they aren't executed as originally planned.

For example, consider an MRI machine with scheduled maintenance plans for both monthly and quarterly. If monthly maintenance occurs on the 15th and quarterly maintenance on the 22nd of every third month, these schedules overlap every three months. Both schedules might include tasks, such as air vents cleaning. To avoid doing the same task twice, a suppression period \(for example, seven days\) is used to check for overlaps. If the monthly tasks are covered in the quarterly schedule, the system suppresses the monthly maintenance. This helps prevent duplication, saves resources, and maintains operational efficiency.

**Note:**

-   To suppress schedules, the planned work schedules must be attached to similar work order templates or include similar tasks.
-   Work orders can be suppressed either fully or partially, depending on the attached work order templates and associated tasks.
-   If all work orders in the planned schedules match, they are fully suppressed and duplicate tasks are removed.
-   If work orders match partially, duplicate work orders for the matching tasks are removed, and work orders are created for the remaining tasks.

The steps to suppress schedule occurrences of your planned work after creating a work plan are:

1.  Customize the time window for the suppression period by selecting the appropriate value for the property sn\_fsm\_planned\_wm.tolerance\_span in [Planned Work Management system properties](../reference/planned_work_management_sys_properties.md).
2.  [Configure a work schedule](../task/configure-work-plan.md)
3.  Associate the work schedule with templates. For more information, see [Associate a work order template to a work schedule](../task/associate-work-schedule-to-wotemplate.md) and [Associate a task plan template to a work schedule](../task/map-schedule-to-task-template.md).
4.  [Create planned work records](../task/create-planned-work-records.md)
5.  [Generate work orders](generate-work-orders.md)
6.  [Suppress schedule occurrences of your planned work](../task/suppress_schedules_of_your_work_plans.md)

