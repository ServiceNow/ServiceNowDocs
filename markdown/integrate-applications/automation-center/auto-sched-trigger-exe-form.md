---
title: Automation Scheduled Trigger Execution form
description: Use the Automation Scheduled Trigger Execution form to define the type of insight trigger and map an insight rule to a new scheduled script in Automation Center.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Automation Center, Workflow Data Fabric]
---

# Automation Scheduled Trigger Execution form

Use the Automation Scheduled Trigger Execution form to define the type of insight trigger and map an insight rule to a new scheduled script in Automation Center.

<table id="table_rtt_sdm_15b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the insight trigger.

</td></tr><tr><td>

Active

</td><td>

Option for ensuring the use of the insight trigger.

</td></tr><tr><td>

Application

</td><td>

The associated application or the application scope in which the trigger is being created, such as Automation Center or RPA Hub.

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

Day

</td><td>

Day on which the scheduled job should run.

-   If **Run** is set to **Weekly**, select the day of the week. For example, select Wednesday.
-   If **Run** is set to **Monthly**, select the day of the month. For example, select 25 for the 25th day of the month.

This field appears only if you select **Monthly** or **Weekly** in the **Run** field.

</td></tr><tr><td>

Repeat Interval

</td><td>

This field appears only if you select **Periodically** in the **Run** field.

 Duration of the repeat interval for each scheduled job execution. Enter the duration in the number of days, hours, or minutes. For example:

-   To run the scheduled job every four days, enter `04` in the **Days** field.
-   To run it every 26 hours, enter `26` in the **Hours** field.
-   If it should repeat at an interval of 13:30:25, enter `13` in the **Hours** field, and then enter `30` and `25` in the two unlabeled fields after it.

</td></tr><tr><td>

Time zone

</td><td>

Time zone to use with the **Time** field entry when you specify the time at which the scheduled job should run. Select a time zone entry:

-   **-None-**: Use the default time zone for the logged-in user who is creating the scheduled job.

For example, the scheduled job runs at 04:45 p.m. US/Pacific time if it’s the user's assigned time zone, and you enter `16:45` into the **Time** field.

-   **Use System Time Zone**: Use the default system time zone that is specified for the instance in which it runs.

For example, the scheduled job runs at 10:15 p.m. London time if Europe/London is the default system time zone for the instance, and you enter `22:15` in the **Time** field.

-   Actual time zone.

For example, the scheduled job runs at 1:30 p.m. in the US Eastern time zone if you select **US/Eastern**, and enter `13:30` in the **Time** field.


</td></tr><tr><td>

Time

</td><td>

Time of day at which the scheduled job should run, expressed in hours, minutes, and seconds on a 24-hour clock. The selection that you make in the **Time zone** field determines the time zone for this entry.

</td></tr><tr><td>

Starting

</td><td>

Allows you to define the beginning window of time when you would like your job to start running. The job will actually run at the time specified in **Run time**. Select the calendar date and time. The **Starting** field appears only if you select one of the following **Run** types in the **Run** field:

</td></tr><tr><td>

Business Calendar

</td><td>

Business calendar entry that you’re using to determine the business calendar start or end date for the scheduled job. This field appears only if you select **Business Entry: Start Date** or **Business Entry: End Date** in the **Time** field.

</td></tr></tbody>
</table>**Parent Topic:**[Automation Center reference](../concept/automation-center-reference.md)

