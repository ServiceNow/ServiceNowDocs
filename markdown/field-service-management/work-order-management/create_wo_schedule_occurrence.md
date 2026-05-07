---
title: Generate work orders for schedule occurrences
description: Generate work orders for schedule occurrences to maintain a record of specific occurrences or maintenance cycles of the schedule.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Generate work orders, Configure work plans, Planned Work Management, Set up work orders and tasks, Configure, Field Service Management]
---

# Generate work orders for schedule occurrences

Generate work orders for schedule occurrences to maintain a record of specific occurrences or maintenance cycles of the schedule.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## About this task

Work orders are generated for a schedule occurrence when the conditions defined in the plan and schedule are met. This can happen automatically through a nightly scheduled background job or manually when you select **Generate work order** within a schedule. The work orders that are generated for each schedule occurrence are mapped to their corresponding schedule occurrence, enabling you to track work performed for each maintenance cycle separately.

The work orders for a schedule occurrence are generated depending on the number of work order templates associated with it. For example, if two work order templates are configured for a work schedule, the system generates two work orders for that particular schedule occurrence, based on each template.

**Note:**

If a lead time is set in the schedule associated with the schedule occurrence, it affects when work can start. **Earliest Start Date** of the schedule occurrence is calculated by subtracting the lead time duration from **Requested By** date \(**Requested Due By** – **Lead Time**\). For example, if **Requested By** is 25 February 2026 and the lead time is 4, **Earliest Start Date** is set to 21 February 2026.

When the work order is generated, the dates are set as follows:

-   **Scheduled Start** is set to the schedule occurrence’s **Earliest Start Date** \(with lead time adjustment\).

-   **Requested Due By** is set to the schedule occurrence's **Requested Due By** date.

-   The **Window start** and **Window end** dates for the associated work order tasks are auto populated with the schedule occurrence's **Earliest Start Date** \(with lead time adjustment\) and **Requested Due By** dates.
-   If the **Scheduled Start** and **Requested Due By** of a work order are identical, by default, the **Window start** duration of the associated work order task is set to one hour prior to the **Requested Due By** duration.

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open the work plan.

3.  In the Planned Work Schedules related list, select the schedule for which you want to review the schedule occurrences.

4.  In the Schedule Occurrences related list, select the schedule occurrence for which you want to create work orders.

5.  In the Related Links section, select **Generate work order**.

6.  View the work orders associated with the event from the Work Orders related list.


## Result

A list of work orders is automatically generated for the selected schedule occurrence, taking into account the number of work order templates associated with the schedule.

**Related topics**  


[Associate a work order template to a work schedule](associate-work-schedule-to-wotemplate.md)

