---
title: Run a scheduled job to execute a planned work schedule
description: Planned work schedules are executed whenever the meter, duration, script, or condition criteria meets. You can also use the Schedule ad-hoc feature to run a maintenance schedule manually.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a work order for the planned work, Manage work orders, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Run a scheduled job to execute a planned work schedule

Planned work schedules are executed whenever the meter, duration, script, or condition criteria meets. You can also use the Schedule ad-hoc feature to run a maintenance schedule manually.

## Before you begin

Role required: admin

## About this task

Planned work schedules run regularly using the **Planned Maintenance Nightly Run** scheduled job. When the scheduled job runs, the appropriate work orders are created for all records that meet the schedule criteria \(including all records for the current day\).

You must configure the nightly planned maintenance schedule job to run the planned work schedule.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Schedule Jobs**.

2.  In the **Search** field, enter **Planned Maintenance Nightly Run**.

3.  Select **Planned Maintenance Nightly Run**.

4.  To specify a different schedule for running the job, change the **Run** and **Time** fields.

    A scheduled job does not run based on the value set in the Next run time field in the maintenance plan record for this job. For more information, see [Configure a work schedule](configure-work-plan.md).

5.  Click **Update**.

6.  At any time, to run the scheduled job, click **Execute Now**.

    **Note:**

    The scheduled job evaluates all previously defined schedules and executes the ones that are scheduled to run.

    If one or more records in the table associated with the work plan are deleted after the matching records were associated with the work plan, the next nightly run removes all the records associated with those removed assets.


**Parent Topic:**[Create a work order for the planned work](../concept/creating-work-orders-from-planned-work.md)

