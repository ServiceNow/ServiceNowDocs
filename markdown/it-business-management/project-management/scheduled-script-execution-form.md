---
title: Scheduled Script Execution Form
description: Use the scheduled script execution form to define a scheduled job.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Form field information for Project Management, Reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Scheduled Script Execution Form

Use the scheduled script execution form to define a scheduled job.

<table id="id_ycz_lpj_2xb"><thead><tr><th>

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

Run

</td><td>

Time interval to use for running the scheduled job:

-   **Daily**: Runs daily, at a designated time.
-   **Weekly**: Runs on a weekly basis, at a designated time and day of the week.
-   **Monthly**: Runs on a monthly basis, at a designated time and day of the month.
-   **Periodically**: Runs on a designated repeating interval.
-   **Once**: Runs for a single occurrence only.
-   **On Demand**: Runs immediately on demand.
-   **Business Calendar: Entry Start**: Runs on the starting entry dates for the business calendar that you select in the **Business Calendar** field. A scheduled job runs for the starting date of each of the business entries that you defined for the business calendar.

For example, if the business calendar represents a fiscal year, and the starting date of each entry is a fiscal month, the scheduled job runs on the first day of each month.

-   **Business Calendar: Entry End**: Runs for the ending date for the business calendar that you select in the **Business Calendar** field. This selection runs in the same manner as **Business Calendar: Entry Start**, but for the end dates of the associated business calendar entries.

**Note:** When you select **Business Calendar: Entry Start** or **Business Calendar: Entry End**, you can apply an offset factor to schedule the job to run before or after the time span of the selected business calendar. To learn more, see the **Offset type** and **Offset** fields.

To learn more about creating and using business calendars and defining business calendar entries, see [Creating business calendars](https://www.servicenow.com/docs/access?context=business-calendars&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and [Define business calendar entries](https://www.servicenow.com/docs/access?context=define-business-calendar-entries&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


</td></tr><tr><td>

Time zone

</td><td>

Time zone to use with the **Time** field entry when you specify the time at which the scheduled job should run. Select a time zone entry:

-   **-None-**: Use the default time zone for the logged-in user who is creating the scheduled job.

For example, the scheduled job runs at 04:45 p.m. US/Pacific time if it is the user's assigned time zone, and you enter `16:45` into the **Time** field.

-   **Use System Time Zone**: Use the default system time zone that is specified for the instance in which it runs.

For example, the scheduled job runs at 10:15 p.m. London time if Europe/London is the default system time zone for the instance, and you enter `22:15` in the **Time** field.

-   Actual time zone.

For example, the scheduled job runs at 1:30 p.m. in the US Eastern time zone if you select **US/Eastern**, and enter `13:30` in the **Time** field.


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

Duration of the repeat interval for each scheduled job execution. Enter the duration in the number of days, hours, or minutes. For example:

-   To run the scheduled job every four days, enter `04` in the **Days** field.
-   To run it every 26 hours, enter `26` in the **Hours** field.
-   If it should repeat at an interval of 13:30:25, enter `13` in the **Hours** field, and then enter `30` and `25` in the two unlabeled fields after it.

 These fields appear only if you select **Periodically** in the **Run** field.

**Note:** This setting does not account for Daylight Saving Time changes. For example, if you select a period of one day, the calculation adds 24 hours to the starting time of the job. If the start time is in a Daylight Saving Time \(DST\) period, the job runs with a one-hour offset when that time zone is not in DST.

</td></tr><tr><td>

Business Calendar

</td><td>

Business calendar entry that you are using to determine the business calendar start or end date for the scheduled job. This field appears only if you select **Business Entry: Start Date** or **Business Entry: End Date** in the **Time** field.

</td></tr><tr><td>

Offset Type

</td><td>

Type of time offset, if any, to apply to the business calendar that you selected for scheduling this job:

-   **Past**: Apply an offset factor to schedule the job to run before the start of the time span of the selected business calendar.
-   **Future**: Apply an offset factor to schedule the job to run after the end of the time span of the selected business calendar.
-   **--None--**: Do not apply a time offset when scheduling this job.

Adding an offset factor enables you to schedule the job to run before, or after, the formal time span that is defined in the business calendar for the following use cases:

 -   Schedule a job at a certain time, outside of the time span for the selected business calendar.
-   Arrange multiple jobs to run in sequence, around the time span of the selected business calendar.

The **Offset type** and **Offset** fields appear only if you select **Business Calendar: Entry Start** or **Business Calendar: Entry End** in the **Run** field.

</td></tr><tr><td>

Offset

</td><td>

Amount of time offset, expressed in days, hours, minutes, and seconds, to apply to the business calendar that you selected for scheduling this job. For example, if you want to schedule the job to start three days, 14 hours, 10 minutes, and 45 seconds before the business calendar start date, do the following actions:

-   Select **Past** in the **Offset type** field.
-   Enter **3** in the **Days** field.
-   Enter **14**, **10**, and **45** in the **Hours** field.

The **Offset Days** and **Hours** fields appear only if you select **Business Calendar: Entry Start** or **Business Calendar: Entry End** in the **Run** field, and **Past** or **Future** in the **Offset type** field.

</td></tr><tr><td>

Time

</td><td>

Time of day at which the scheduled job should run, expressed in hours, minutes, and seconds on a 24-hour clock. The selection that you make in the **Time zone** field determines the time zone for this entry. **Note:** Time values are always saved in the ServiceNow AI Platform® in UTC time and then translated into the proper time. This translation depends on the selected **Time zone** and the entry in the **Time** field.

 This field appears only if you select **Daily**, **Weekly**, or **Monthly** in the **Run** field.

</td></tr><tr><td>

Starting

</td><td>

Date and time of the first scheduled job generation. Select the calendar date and time. This field appears only if you select **Periodically** in the **Run** field.

</td></tr><tr><td>

Priority

</td><td>

Numerical priority for the scheduled job:

-   Set essential jobs to a priority value below 100.
-   Set nonessential jobs to a priority above 100.
-   If 70 percent or more of all scheduled jobs are **Overdue**, any jobs that are marked with a value above 100 do not run.

</td></tr><tr><td>

Run as

</td><td>

Name of the user who is creating and running the scheduled job. To assign the scheduled job to the system instead of the person creating the scheduled job, create a system or dummy user and add it to this field.

</td></tr><tr><td>

Conditional

</td><td>

Option for enabling the running of the scheduled job if certain conditions are met in the associated script.

</td></tr><tr><td>

Condition

</td><td>

Conditional script that determines if a scheduled job should run. The last expression of the script should evaluate to a Boolean \(true/false\) value. This text box appears only if you select **Use conditions**.

</td></tr><tr><td>

Starting

</td><td>

Date and time of the first scheduled job generation. Select the calendar date and time. This field appears only if you select **Periodically** in the **Run** field.

</td></tr></tbody>
</table>**Related topics**  


[Generate labor costs](../task/gen-cost-pln-prj-wrkspc.md)

[Activate a scheduled job to generate labor costs](../task/gen-labor-costs-scheduled-job-ppm.md#)

