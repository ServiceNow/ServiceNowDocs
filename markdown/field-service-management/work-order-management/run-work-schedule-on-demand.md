---
title: Run a planned work schedule on demand
description: Planned work schedules mainly run using the Planned Maintenance Nightly Run scheduled job. However, you can make the schedule to run immediately or change the date when a schedule should run, if needed.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage a work order for the planned work, Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Run a planned work schedule on demand

Planned work schedules mainly run using the **Planned Maintenance Nightly Run** scheduled job. However, you can make the schedule to run immediately or change the date when a schedule should run, if needed.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## About this task

When you run a planned work schedule on demand, all of the next run dates for the relevant planned work records are updated to the user-defined time, now or in the future. All the appropriate work orders are created. If the schedule is meter, condition, or script-based, work orders are created for work plan records that meet the schedule criteria.

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open a work plan that contains the schedule to run.

3.  In the Planned Work Schedules related list, select the maintenance schedule you want to run.

4.  In the Related Link section, select **Run on demand**.


