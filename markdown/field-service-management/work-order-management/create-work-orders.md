---
title: Generate work orders
description: Generate work orders for the schedule occurrence either manually or by configuring an automated job.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-02-02"
reading_time_minutes: 1
breadcrumb: [Work plans, Planned Work Management, Work orders and tasks, Configure, Field Service Management]
---

# Generate work orders

Generate work orders for the schedule occurrence either manually or by configuring an automated job.

When a work order and its associated tasks are generated, the start and end dates are set considering the lead time and earliest start date mentioned in the schedule.

If a lead time is set in the schedule associated with the schedule occurrence, it affects when work can start. **Earliest Start Date** of the schedule occurrence is calculated by subtracting the lead time duration from **Requested By** date \(**Requested Due By** – **Lead Time**\). For example, if **Requested By** is 25 February 2026 and the lead time is 4, **Earliest Start Date** is set to 21 February 2026.

When the work order is generated, the dates are set as follows:

-   **Scheduled Start** is set to the schedule occurrence’s **Earliest Start Date** \(with lead time adjustment\).

-   **Requested Due By** is set to the schedule occurrence's **Requested Due By** date.

-   The **Window start** and **Window end** dates for the associated work order tasks are auto populated with the schedule occurrence's **Earliest Start Date** \(with lead time adjustment\) and **Requested Due By** dates.
-   If the **Scheduled Start** and **Requested Due By** of a work order are identical, by default, the **Window start** duration of the associated work order task is set to one hour prior to the **Requested Due By** duration.

To run a scheduled job to generate work orders, see [Run a scheduled job to execute a planned work schedule](../task/run-schedule-job-planned-work.md).

To generate work orders manually, see [Generate work orders for schedule occurrences](../task/create_wo_schedule_occurrence.md).

