---
title: Run a planned work schedule on demand
description: Planned work schedules mainly run using the Planned Maintenance Nightly Run scheduled job. However, you can make the schedule to run immediately or change the date when a schedule should run, if needed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing work orders for the planned work, Using Field Service Management, Field Service Management]
---

# Run a planned work schedule on demand

Planned work schedules mainly run using the **Planned Maintenance Nightly Run** scheduled job. However, you can make the schedule to run immediately or change the date when a schedule should run, if needed.

## Before you begin

Role required: admin

## About this task

When you run a planned work schedule on demand, all of the next run dates for the relevant planned work records are updated to the user-defined time, now or in the future. All the appropriate work orders are created. If the schedule is meter, condition, or script-based, work orders are created for work plan records that meet the schedule criteria.

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Planned Work Management** &gt; **Plans**.

2.  Open a work plan that contains the schedule to run.

3.  In the Planned Work Schedules related list, select the maintenance schedule you want to run.

4.  In the Related Link section, click **Run on demand**.

5.  On the form, fill in the fields.

<table id="table_ax2_dkn_25b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run now

</td><td>

Option to run the maintenance for the schedule immediately.

</td></tr><tr><td>

Select next run date

</td><td>

Date in the future for maintenance to run.This field appears only when the **Run now** option is not selected.

</td></tr></tbody>
</table>6.  Click **Schedule**.


**Parent Topic:**[Managing work orders for the planned work](../concept/creating-work-orders-from-planned-work.md)

