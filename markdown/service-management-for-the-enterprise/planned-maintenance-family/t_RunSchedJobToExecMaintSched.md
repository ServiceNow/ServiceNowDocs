---
title: Run a scheduled job to execute a maintenance schedule
description: Maintenance schedules are executed whenever the meter, duration, script, or condition criteria is met. You can also use the Schedule ad-hoc feature to run a maintenance schedule manually.
locale: en-US
release: zurich
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing maintenance plans, Planned Maintenance, Service Management]
---

# Run a scheduled job to execute a maintenance schedule

Maintenance schedules are executed whenever the meter, duration, script, or condition criteria is met. You can also use the Schedule ad-hoc feature to run a maintenance schedule manually.

## Before you begin

Role required: SM admin

## About this task

Maintenance schedules are run regularly using the Planned Maintenance Nightly Run scheduled job. When the scheduled job is run, the appropriate Service Orders are created for all records that meet the schedule criteria \(including all records for the current day\).

To configure the nightly planned maintenance scheduled job:

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open **Planned Maintenance Nightly Run**.

3.  In Related Links, click **Configure Job Definition**.

4.  To specify a different schedule for running the job, change the **Run** and **Time** fields.

    A scheduled job does not run based on the value set in the **Next run time** field in the maintenance plan record for this job. For more information, see [Configure a maintenance schedule](t_DefineAMaintSched.md).

5.  Click **Update**.

6.  At any time, to run the scheduled job, click **Execute Now**.

    The scheduled job evaluates all previously defined schedules and executes the ones that are scheduled to run.

    **Note:** If one or more records in the table associated with the maintenance plan are deleted after the matching records were associated with the maintenance plan, the next nightly run removes all the records associated with those removed assets.


**Parent Topic:**[Managing maintenance plans](../concept/c_MaintPlanMgmt.md)

