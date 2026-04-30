---
title: Configure a work schedule
description: After creating a work plan, it’s important to define specific criteria to determine when the plan should be executed. This includes defining the start date and end date for the plan's execution. To create a flexible work schedule for the plan, you can configure multiple work schedules for it and assign them accordingly.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Configuring work plans, Configuring Planned Work Management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Configure a work schedule

After creating a work plan, it’s important to define specific criteria to determine when the plan should be executed. This includes defining the start date and end date for the plan's execution. To create a flexible work schedule for the plan, you can configure multiple work schedules for it and assign them accordingly.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin and model\_manager

You must create a work plan before configuring a work schedule for the plan.

## About this task

You can create a single schedule or multiple schedules. For example, you can set up schedules for a class of computer to be rebooted on the first and 15th of every month.

**Note:** Plan carefully when defining multiple work schedules for the same plan. For example, you set up one schedule to replace a printer cartridge every three months. You set up another schedule to replace the cartridge after every 10,000 pages is printed. This conflict could cause the cartridge to be replaced twice in the same week. Ensure that your schedules don’t conflict with one another.

Work schedules can be based on either duration or meter and can be triggered by the first occurring related condition. For example, on the Planned Work Schedule form, select **Duration or Meter** as the trigger for an automobile maintenance schedule and then define the duration as six months and the meter as 10,000 miles. The schedule is triggered by whichever comes first. With the **Duration or Meter** trigger selected, the **Next run time** and **Next run value** fields are populated in the **Planned Work Records** related list on the Work Plan form.

**Note:** In a work plan record, the timestamp displayed in the **Next run time** field isn’t the same as the time set for executing the planned work. The **Next action** field in the **Planned Maintenance Nightly Run** record displays the actual scheduled job execution time for the planned work.

When the scheduled job runs, it checks whether the value in the **Next run time** field is less than the time set for the next planned work nightly run job and if it is, the system generates a request. A planned nightly maintenance isn’t executed and a request isn’t generated based on the next run time.

A flexible work schedule can be created for multiple assets that belong to the same work plan based on their installation date. For example, on the Planned Work Schedule form, select **Field Value** as the start planned schedule based on, for multiple assets and then select **Installed** as the effective start reference. The schedule identifies the starting date of the planned work record based on the installation date of the assets that are associated with the work plan. With the **Field Value** start planned schedule based on selected, the **Next run time** field is populated in the **Planned Work Records** related list on the Work Plan form.

You can also create planned work schedules through the Planned Work Management Workspace. Navigate to **All** &gt; **Planned Work Management** &gt; **Workspace**, and then select the **List** icon \(![List icon.](../image/ListIcon.png)\).

## Procedure

1.  Navigate to **All** &gt; **Planned Work Management** &gt; **Work Plans**.

2.  Open the work plan that you want to associate with a work schedule.

3.  In the **Planned Work Schedules** related list, select New.

4.  On the form, fill in the fields.

<table id="table_rzc_zpy_d5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the planned work schedule.

</td></tr><tr><td>

Short description

</td><td>

Brief summary of the planned work schedule.

</td></tr><tr><td>

Trigger

</td><td>

Timing condition that triggers the execution of the plan. -   **Duration:** work to be performed based on time. Depending on your selection, additional fields appear to define the duration.
-   **Meter:** work to be performed based on count. The **Every** and **Field** fields appear.
-   **Condition:** Maintenance to be performed when a certain condition is met. The **Filter Condition** field appears.
-   **Script:** Apply advanced criteria for running a maintenance plan. The **Script** field appears.
-   **Duration or Meter:** Maintenance to be performed based on both time and count, whichever comes first. You must specify the duration and meter details.


</td></tr><tr><td>

Plan

</td><td>

Name of the work plan that this schedule is a part of.This field is automatically set to the name of the work plan.

</td></tr><tr><td>

Active

</td><td>

Option to enable the schedule for a work plan.

</td></tr><tr><td class="sub-head" colspan="2">

Duration Details

</td></tr><tr><td>

Trigger type

</td><td>

Duration category for the work schedule. For example, if you select **Multiple days of the week**, the **Due days of week** field appears so you can specify on which days in a week planned work should be performed. Different fields appear depending on the trigger type selected. This field appears when **Duration** is selected for **Trigger**.

</td></tr><tr><td>

Monthly type

</td><td>

Select either Fixed or Floating to mention a particular day of the month to run the schedule.This field appears when the **Trigger type** field is set to **Monthly**.

</td></tr><tr><td>

Annually type

</td><td>

Select either Fixed or Floating to specify a particular day and month in a year to run the schedule. This field appears only when the **Trigger type** field is set to **Annually**.

</td></tr><tr><td>

Repeat every

</td><td>

Specify how often the schedule should repeats. For example, if you select weekly repetitions, specify the frequency such as every week or every two weeks.

</td></tr><tr><td>

Repeat

</td><td>

Frequency of the planned work schedule to repeat. This field appears when the **Trigger type** field is set to **Interval**.

</td></tr><tr><td>

Due day of week

</td><td>

Day of week to repeat on. This field appears when **Weekly** is selected for **Trigger type**.

</td></tr><tr><td>

Due day of month

</td><td>

Day of the month to repeat on. This field appears when **Monthly** or **Annually** is selected for **Trigger type**.

</td></tr><tr><td>

Due month

</td><td>

Month to repeat on. This field appears when **Annually**is selected for **Trigger type**.

</td></tr><tr><td>

Due time

</td><td>

Time of day in hours, minutes, and seconds. This field appears for all trigger types except Interval.

</td></tr><tr><td>

Lead time

</td><td>

Number of days prior to the **Requested Due by** date to determine the date on which work should begin. That date is pre-filled in the **Scheduled start** field for the task. This field appears when **Duration** is selected for **Trigger**.

</td></tr><tr><td>

Preserve calculated interval

</td><td>

Option to restart the interval calculation from the time that the work order was completed.This field appears when **Interval**, **Monthly**, or **Annually** is selected for **Trigger type** and **Fixed** is selected for the **Monthly type** and **Annually type** field.

</td></tr><tr><td>

Condition

</td><td>

Condition that determines if the maintenance schedule should run.This field appears when **Condition** is selected for Trigger.

</td></tr><tr><td>

Script

</td><td>

Script that determines if the maintenance schedule should run. For example, Maintenance runs if the script returns true. The "current" variable is available and represents the record that is undergoing maintenance, for example, a CI.This field appears when **Script** is selected for **Trigger**.

</td></tr><tr><td class="sub-head" colspan="2">

Meter Details

</td></tr><tr><td>

Table

</td><td>

Lists the table associated with the assets or CIs selected for maintenance. This field appears when Meter or Condition is selected for Trigger.

</td></tr><tr><td>

Field

</td><td>

Field used to define what the occurrences in the **Every** field apply to. For example, if the pages field is entered, the **Every** field can contain the number of pages that are printed before the action defined in the plan is performed. This field appears when **Meter** is selected for Trigger.

</td></tr><tr><td>

Every

</td><td>

Number of occurrences, such as miles or pages that must be recorded before the work plan is executed. The value must be greater than zero \(0\).This field appears when **Meter** is selected for Trigger.

</td></tr><tr><td>

Preserve calculated meter

</td><td>

Option to restart the meter calculation based on the value defined in the **Every** field.

</td></tr><tr><td class="sub-head" colspan="2">

Effectivity Details

</td></tr><tr><td>

Start planned schedule based on

</td><td>

Option based on which the planned work schedule should determine its start date.-   Date
-   Field Value
-   Schedule


</td></tr><tr><td>

Effective Start

</td><td>

Effective start date from when the planned work is scheduled to work.

</td></tr><tr><td>

Effective start reference

</td><td>

Field value that should be used to determine the start date of the planned work. Effective start reference displays the list of fields from the table that is selected to create conditions for the work plan. For example, Printer \[cmdb\_ci\_printer\]This field appears only when **Field Value** is selected from **Start planned schedule based on**.

</td></tr><tr><td>

Schedule

</td><td>

Name of the schedule that should be used to calculate the start date of the work plan.This field appears only when **Schedule** is selected from **Start planned schedule based on**.

</td></tr><tr><td>

End planned schedule based on

</td><td>

Value that determines the end date of a planned work schedule.-   Date
-   Field Value
-   Frequency


</td></tr><tr><td>

Frequency

</td><td>

Determine how often the planned work is scheduled to be performed. For example, if frequency is mentioned as 4, the planned work cycle will run for four times and ends after the fourth iteration.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

The schedule is created for a work plan. The Schedule Occurrences related list is added to the schedule to track the occurrence of maintenance cycles for the schedule.

The schedule occurrences are created automatically for duration-based schedules. However, if a different trigger option is selected for a schedule, the occurrence is created only when the specified condition or meter value is met. The creations of schedule occurrences depend on the effective end date. If no effective end date is specified, the application generates the next occurrence of the schedule.

