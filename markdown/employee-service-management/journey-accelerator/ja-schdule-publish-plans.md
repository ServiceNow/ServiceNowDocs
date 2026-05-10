---
title: Modify a scheduled job for Publish Journey Accelerator plans
description: Update the Publish Journey Accelerator plans job. The job evaluates a plan's publish date to determine when to publish the plan.
locale: en-US
release: australia
product: Journey Accelerator
classification: journey-accelerator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Modify a scheduled job for Publish Journey Accelerator plans

Update the Publish Journey Accelerator plans job. The job evaluates a plan's publish date to determine when to publish the plan.

## Before you begin

Role required: admin

## About this task

You can change the scheduled frequency at which the job runs, modify scripts, and add conditions.

**Note:** The default scheduled frequency for a Publish Journey Accelerator plan is 12 hours.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the **Name** field, enter `Publish Journey Accelerator plans`, press **Enter**, and then open the job.

3.  On the form, fill in the fields.

<table id="t_ScheduleScriptExecution"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that identifies this scheduled job.

</td></tr><tr><td>

Active

</td><td>

Option that indicates that scheduled job is active and should be executed at the specified date and time.

</td></tr><tr><td>

Application

</td><td>

Name of the application that contains the script. **Global** appears if the script is in the global scope.

</td></tr><tr><td>

Conditional

</td><td>

Option for enabling the running of the scheduled job if certain conditions are met in the associated script.

</td></tr><tr><td>

Run

</td><td>

Time interval to use for running the scheduled job:

-   **Daily**: Runs daily, at a designated time.
-   **Day and Month in Year**: Runs yearly on a specific day and month \(for example, July 14\), at a designated time.
-   **Day in Week in Month in Year**: Runs yearly on a specific day of the week in a specific week of a specific month \(for example, the second Monday in October\), at a designated time.
-   **Week in Month**: Runs monthly during a specific week of the month \(for example, the third week of each month\), on designated days and at a designated time.
-   **Weekly**: Runs on a weekly basis, at a designated time and day of the week.
-   **Monthly**: Runs on a monthly basis, at a designated time and day of the month.
-   **Periodically**: Runs on a designated repeating interval.
-   **Once**: Runs for a single occurrence only.
-   **On Demand**: Runs immediately on demand.
-   **Business Calendar: Entry Start**: Runs on the starting entry dates for the business calendar that you select in the **Business Calendar** field. A scheduled job runs for the starting date of each of the business entries that you defined for the business calendar.

For example, if the business calendar represents a fiscal year, and the starting date of each entry is a fiscal month, the scheduled job runs on the first day of each month.

-   **Business Calendar: Entry End**: Runs for the ending date for the business calendar that you select in the **Business Calendar** field. This selection runs in the same manner as **Business Calendar: Entry Start**, but for the end dates of the associated business calendar entries.

**Note:** When you select **Business Calendar: Entry Start** or **Business Calendar: Entry End**, you can apply an offset factor to schedule the job to run before or after the time span of the selected business calendar. If you select a business calendar and all its business calendar spans are in the past, the job would never run since that is an invalid configuration. To learn more, see the **Offset type** and **Offset** fields.

To learn more about creating and using business calendars and defining business calendar entries, see [Creating business calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/business-calendars.md) and [Define business calendar entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/define-business-calendar-entries.md).

</td></tr><tr><td>

Repeat Interval

</td><td>

Duration of the repeat interval for each scheduled job execution. Enter the duration in the number of days, hours, or minutes. For example:

-   To run the scheduled job every four days, enter `04` in the **Days** field.
-   To run it every 26 hours, enter `26` in the **Hours** field.
-   If it should repeat at an interval of 13:30:25, enter `13` in the **Hours** field, and then enter `30` and `25` in the two unlabeled fields after it.


</td></tr><tr><td>

Starting

</td><td>

Allows you to define the beginning window of time when you would like your job to start running. The job will actually run at the time specified in **Run time**. Select the calendar date and time. The **Starting** field appears only if you select one of the following **Run** types in the **Run** field:

</td></tr><tr><td>

Condition

</td><td>

A conditional script that determines if a scheduled job should run. The last expression of the script should evaluate to a Boolean \(true/false\) value. This text box appears only if you select **Use conditions**.

</td></tr><tr><td>

Run this script

</td><td>

Name of the script to run at the scheduled date and time. Two examples are copy script logic from a business rule or call a script include.

</td></tr></tbody>
</table>4.  Click **Update**.

    To learn more about scheduled jobs, see [Scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ScheduledJobs.md).


