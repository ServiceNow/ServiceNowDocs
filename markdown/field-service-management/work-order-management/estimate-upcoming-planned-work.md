---
title: Generate work orders for upcoming days
description: Determine work orders in advance for the upcoming period in future, for example, for the next 30 days, one year, or more. It helps to plan the work force and required parts for the upcoming planned work. This provides long term visibility into upcoming workload and supports proactive planning.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a work order for the planned work, Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Generate work orders for upcoming days

Determine work orders in advance for the upcoming period in future, for example, for the next 30 days, one year, or more. It helps to plan the work force and required parts for the upcoming planned work. This provides long term visibility into upcoming workload and supports proactive planning.

## Before you begin

Ensure that forecasting is enabled and the future time window is defined.

-   Select the **Forecast work orders** check box in the Work Plan form to enable forecasting.
-   In the planned work schedule specify the **Days in future to create work orders** to control how far ahead work orders are created.

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## About this task

By default, Planned Work Management generates only the next immediate work order for a schedule. When forecasting is enabled, the system automatically generates multiple future work orders beyond the next scheduled execution, up to the configured number of days in the future.

This provides long-term visibility into upcoming work and supports proactive planning for technicians, parts, and materials.

The timing of work order generation is controlled using Lead Time and Days in Future to Generate Work Orders. For each schedule occurrence, the system checks whether the current date \(the day on which the job runs\) is later than or same as the date calculated by the formula `Requested Due By date – Lead Time – Days in Future`. When this condition is satisfied, the work order is automatically generated. This ensures that work orders are created neither too early nor too late, and become available at the right time for planning and execution.

**Note:** The nightly job can be customized. For more information, see [Run a scheduled job to execute a planned work schedule](run-schedule-job-planned-work.md).

You can also create planned work orders through the Planned Work Management Workspace. Navigate to **All** &gt; **Planned Work Management** &gt; **Workspace**, and then click the List icon \(![List icon.](../image/ListIcon.png)\).

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open a desired plan from the list of work plans.

3.  In the Planned Work Schedules related list, select a schedule to which you want to associate a work order template.

4.  In the Related Links section, click **Generate work order**.


## Result

A list of work orders is auto-generated for the selected period in future.

