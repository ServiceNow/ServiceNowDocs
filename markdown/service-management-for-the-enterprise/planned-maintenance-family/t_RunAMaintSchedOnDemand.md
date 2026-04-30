---
title: Run a maintenance schedule on demand
description: Maintenance schedules are typically run using the scheduled job named Planned Maintenance Nightly Run. However, you may want to run the schedule immediately or change the date when a schedule runs.
locale: en-US
release: zurich
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing maintenance plans, Planned Maintenance, Service Management]
---

# Run a maintenance schedule on demand

Maintenance schedules are typically run using the scheduled job named Planned Maintenance Nightly Run. However, you may want to run the schedule immediately or change the date when a schedule runs.

## Before you begin

Role required: admin

## About this task

When you run a maintenance schedule on demand, all of the next run dates for the relevant maintenance plan records are updated to the user-defined time, now or in the future. All the appropriate service orders are created. If the schedule is meter, condition, or script-based, service orders are created for maintenance plan records that meet the schedule criteria.

## Procedure

1.  Navigate to **All** &gt; **Planned Maintenance** &gt; **Maintenance Plans**.

2.  Open the Maintenance Plan that contains the schedule to run.

3.  In the **Maintenance Schedules** related list, select the maintenance schedule you want to run.

4.  Click the **Run on demand** related link and then fill in the form.

<table id="table_upp_ml3_ts"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run now

</td><td>

Select the check box to run the maintenance for the schedule immediately. Clear the check box to schedule a date for the schedule to run.

</td></tr><tr><td>

Select date

</td><td>

Date in the future for maintenance to run. **Note:** This field appears only when the **Run Now** check box is not selected.

</td></tr></tbody>
</table>
**Parent Topic:**[Managing maintenance plans](../concept/c_MaintPlanMgmt.md)

