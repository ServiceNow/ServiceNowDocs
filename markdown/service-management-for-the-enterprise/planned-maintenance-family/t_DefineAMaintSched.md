---
title: Configure a maintenance schedule
description: After creating a maintenance plan, define specific criteria for determining when the plan should be executed.
locale: en-US
release: xanadu
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Managing maintenance plans, Planned Maintenance, Service Management]
---

# Configure a maintenance schedule

After creating a maintenance plan, define specific criteria for determining when the plan should be executed.

## Before you begin

Role required: sm\_admin

## About this task

Depending on the asset or CI for which you are setting up maintenance plans, you can create a single plan or multiple plans. For example, you can set up plans for a class of computer to be rebooted on the first and fifteenth of every month.

**Note:** Plan carefully when defining multiple maintenance schedules for the same plan. For example, you set up one schedule to replace a printer cartridge every three months. You set up another schedule to replace the cartridge after every 10,000 pages is printed. This conflict could cause the cartridge to be replaced twice in the same week. Ensure that your schedules do not conflict with one another.

Based on the templates associated with the plan, one or more service management work orders and facilities requests are auto-generated.

Maintenance schedules can be based on either duration or meter and can be triggered by the first occurring related condition. For example, on the Maintenance Schedule form, select **Duration or Meter** as the trigger for an automobile maintenance schedule and then define the duration as three months and the meter as 5,000 miles. The schedule is triggered by whichever comes first. With the **Duration or Meter** trigger selected, the **Next run time** and **Next run value** fields are populated in the **Maintenance Plan Records** related list on the Maintenance Plan form.

**Note:** In a maintenance plan record, the time stamp displayed in the **Next run time** field is not the same as the time set for executing the planned maintenance. The **Next action** field in the **Planned Maintenance Nightly Run** record displays the actual scheduled job execution time for the planned maintenance.

When the scheduled job runs, it will check whether the value in the **Next run time** field is less than the time set of the next planned maintenance nightly run job and if it is, the system will generate a request. A planned nightly maintenance is not executed and a request is not generated based on the next run time.

## Procedure

1.  Navigate to **All** &gt; **Planned Maintenance** &gt; **Maintenance Plans**.

2.  Click the number of the maintenance plans you want to associate to a maintenance schedule.

3.  In the **Maintenance Schedules** related list, click **New**, specify a meaningful **Name** and **Short description**, fill in the form, and then click **Submit**.

    **Note:** If the form is configured to show the **Next action** field, you can select the date and time for the first maintenance to be performed.

<table id="table_apw_f2w_mr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Plan

</td><td>

Name of the maintenance plan that this schedule is a part of.

</td></tr><tr><td>

Active

</td><td>

Select the check box to activate the schedule for the maintenance plan.

</td></tr><tr><td>

Trigger

</td><td>

Timing condition that triggers the execution of the plan.

-   **Duration**: Maintenance to be performed based on time. Depending on your selection, additional fields appear to define the duration.
-   **Meter**: Maintenance to be performed based on count. The **Every** and **Field** fields appear.
-   **Condition**: Maintenance to be performed when a certain condition is met. The **Filter condition** field appears
-   **Script**: Apply advanced criteria for running a maintenance plan. The **Script** field appears.
-   **Duration or Meter**: Maintenance to be performed based on both time and count, whichever comes first. You must specify the duration and meter details.


</td></tr><tr><td>

Trigger type

</td><td>

Duration category for the maintenance schedule. For example, if you select **Monthly**, the **Due day of month** field appears so you can specify which day of each month to run maintenance. Different fields appear depending on the trigger type selected. This field appears when **Duration** is selected for **Trigger**.

</td></tr><tr><td>

Repeat

</td><td>

Frequency of the repetition. This field appears when **Interval** is selected for **Trigger type**.

</td></tr><tr><td>

Due day of week

</td><td>

Day of week to repeat on. This field appears when **Weekly** is selected for **Trigger type**.

</td></tr><tr><td>

Due day of month

</td><td>

Day of the month to repeat on. This field appears when **Monthly** or **Annually**is selected for **Trigger type**.

</td></tr><tr><td>

Due month

</td><td>

Month to repeat on. This field appears when **Annually** is selected for **Trigger type**.

</td></tr><tr><td>

Due time

</td><td>

Time of day in hours, minutes, and seconds. This field appears for all trigger types except **Interval**.

</td></tr><tr><td>

Every

</td><td>

Number of occurrences, such as miles or pages, that must be recorded before the maintenance plan is executed. Must be greater than zero \(0\). This field appears when **Meter** is selected for **Trigger**.

</td></tr><tr><td>

Field

</td><td>

Field used to define what the occurrences in the **Every** field apply to. For example, if the **pages** field is entered, the **Every** field can contain the number of pages that are printed before the action defined in the plan is performed. This field appears when **Meter** is selected for **Trigger**.

</td></tr><tr><td>

Table

</td><td>

Lists the table associated with the assets or CIs selected for maintenance. This field appears when **Meter** or **Condition** is selected for **Trigger**.

</td></tr><tr><td>

Lead time

</td><td>

Number of days prior to the **Requested Due by** date to determine the date on which work should begin. That date is pre-filled in the **Scheduled start** field for the task. This field appears when **Duration** is selected for **Trigger**.

</td></tr><tr><td>

Condition

</td><td>

Condition that determines if the maintenance schedule should run. This field appears when Condition is selected for **Trigger**.

</td></tr><tr><td>

Script

</td><td>

Script that determines if the maintenance schedule should run. This field appears when Script is selected for **Trigger**. Maintenance runs if the script returns true. The "current" variable is available and represents the record that is undergoing maintenance, for example, a CI.

</td></tr></tbody>
</table>4.  Specify whether the next planned maintenance should occur at the originally calculated time/meter value or whether to restart the meter/interval calculation from the time that the work order was completed.

    See [Property settings for Planned Maintenance](../reference/planned-maint-properties.md).


-   **[Changes to maintenance schedules](../concept/c_ChangesToMaintSched.md)**  
If you make and save changes to an existing maintenance schedule, any previously associated records are updated accordingly.

**Parent Topic:**[Managing maintenance plans](../concept/c_MaintPlanMgmt.md)

