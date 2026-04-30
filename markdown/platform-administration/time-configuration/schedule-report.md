---
title: Automate generation and distribution of a report
description: Generate and distribute scheduled reports via email.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Create a scheduled job, Scheduled jobs, System scheduler, Explore, Time configuration, Configure core features, Administer]
---

# Automate generation and distribution of a report

Generate and distribute scheduled reports via email.

## Before you begin

Roles required: admin

A user with the report\_scheduler role can also create a scheduled report through a different navigation path. For more information, see [Schedule emails of Core UI reports](https://www.servicenow.com/docs/access?context=t_ScheduleAReport&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

## About this task

Scheduled reports can be distributed in PDF, CSV, or XLS format. Graphical reports can be distributed in PNG or PDF format. Multilevel pivot reports can only be scheduled in PDF format.

**Note:**

-   It is not possible to schedule Calendar, Map, or Single Score reports. You can schedule Pivot Table reports only if the plug-in **com.snc.whtp** is enabled.
-   Data may not appear on reports created by an individual whose user account is deactivated. To ensure that the desired data appears, an active user must recreate the scheduled report.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select **New**.

3.  Select **Automate the generation and distribution of a report**.

4.  Populate the following fields:

<table id="table_a2v_qyg_mp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the scheduled report.

</td></tr><tr><td>

Report

</td><td>

Reference to the report you are scheduling. You can use the Search icon ![Search icon](../../search-administration/image/SearchIcon.png) to locate the report.**Note:** Automatic email support is not available for Calendar, Map, and Single Score reports.

</td></tr><tr><td>

Users

</td><td>

Individual users who receive the report at the scheduled date and time. Users must have **Notification** set to **Enabled** on their user records to receive reports.

</td></tr><tr><td>

Groups

</td><td>

Groups that receive the report at the scheduled date and time.

</td></tr><tr><td>

Email addresses

</td><td>

Comma-separated list of email addresses of report recipients who are not users on your instance.

</td></tr><tr><td>

Application

</td><td>

Name of the scoped application that contains the report. **Global** appears if the report is in the global scope.

</td></tr><tr><td>

Active

</td><td>

When active, scheduled reports are delivered.

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

To learn more about creating and using business calendars and defining business calendar entries, see [Creating business calendars](../../time/concept/business-calendars.md) and [Define business calendar entries](../../time/task/define-business-calendar-entries.md#).

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


</td></tr><tr><td>

Starting

</td><td>

Allows you to define the beginning window of time when you would like your job to start running. The job will actually run at the time specified in **Run time**. Select the calendar date and time. The **Starting** field appears only if you select one of the following **Run** types in the **Run** field:-   **Daily**
-   **Day and Month in Year**
-   **Day in Week in Month in Year**
-   **Monthly**
-   **Once**
-   **Periodically**
-   **Week in Month**
-   **Weekly**
For the run type **Periodically**, the **Starting** time is the date and time of the first scheduled job generation.

</td></tr><tr><td>

Business Calendar

</td><td>

Business calendar entry that you’re using to determine the business calendar start or end date for the scheduled job. This field appears only if you select **Business Entry: Start Date** or **Business Entry: End Date** in the **Time** field.

</td></tr><tr><td>

Offset type

</td><td>

Type of time offset, if any, to apply to the business calendar that you selected for scheduling this job:

-   **Past**: Apply an offset factor to schedule the job to run before the start of the time span of the selected business calendar.
-   **Future**: Apply an offset factor to schedule the job to run after the end of the time span of the selected business calendar.
-   **--None--**: Don’t apply a time offset when scheduling this job.
Adding an offset factor enables you to schedule the job to run before or after the formal time span that is defined in the business calendar for the following use cases:

</td></tr><tr><td>

Offset

</td><td>

Amount of time offset, expressed in days, hours, minutes, and seconds, to apply to the business calendar that you selected for scheduling this job. For example, if you want to schedule the job to start three days, 14 hours, 10 minutes, and 45 seconds before the business calendar start date, do the following actions:

-   Select **Past** in the **Offset type** field.
-   Enter **3** in the **Days** field.
-   Enter **14**, **10**, and **45** in the **Hours** field.
The **Offset Days** and **Hours** fields appear only if you select **Business Calendar: Entry Start** or **Business Calendar: Entry End** in the **Run** field, and **Past** or **Future** in the **Offset type** field.

</td></tr><tr><td>

Priority

</td><td>

Numerical priority for the scheduled job:

-   Set essential jobs to a priority value below 100.
-   Set nonessential jobs to a priority above 100.
-   If 70 percent or more of all scheduled jobs are **Overdue**, any jobs that are marked with a value above 100 don’t run.


</td></tr><tr><td>

Conditional

</td><td>

When enabled, specify a scripted condition for generating the report.

</td></tr><tr><td>

Omit if no records

</td><td>

When enabled, empty reports are not distributed.

</td></tr><tr><td>

Condition

</td><td>

A conditional script that determines if a scheduled job should run. The last expression of the script should evaluate to a Boolean \(true/false\) value. This text box appears only if you select **Use conditions**. For more information about scripts on the ServiceNow platform, see [Scripts](https://www.servicenow.com/docs/access?context=c_Script&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).**Warning:** Conditional scripts for scheduled emails are executed in the sandbox. Therefore, function definitions are not allowed. Some API calls and keywords are also not allowed. For more information, see Script sandbox property.

</td></tr><tr><td>

Subject

</td><td>

Text that appears in the subject line of the distribution email.

</td></tr><tr><td>

Introductory message

</td><td>

\(Optional\) Add a message to the report. If the report output type is Embedded PNG,

-   Use the tag `${report:png}` in the message body to position the report in the message. Otherwise, the report appears at the bottom of the message.
-   Use the tag `${report:include_with}` to position other reports included with the email. Otherwise, these reports appear at the bottom of the message.


</td></tr><tr><td>

Type

</td><td>

Report output type. Graphical reports can be PNG or PDF files. List reports can be PDF, Excel, or CSV files.When scheduling a graphical report, select the output type **PDF** or **PDF-landscape** to include the chart grid data. When scheduling a List report, select output type **Excel** or **CSV**.

Select **Embedded PNG** to embed the report visualization in the body of the email. Large images are scaled to fit the email.

For more information, see the section Report output formats.

**Note:** It is only possible to schedule multilevel pivot reports in PDF output.

</td></tr><tr><td>

Zip output

</td><td>

When selected, the report is sent as a zip file attachment to the email.

</td></tr><tr><td>

Include with

</td><td>

One or more additional reports to include with the email. It is not possible to order the reports within the email. You can use the Search icon ![Search icon](../../search-administration/image/SearchIcon.png) to locate the additional reports.

</td></tr><tr><td>

Page size \(Multilevel pivot report only\)

</td><td>

Choose from A3, A4, Letter, or Legal size. To specify a different paper size, select **Custom** and enter the **Page height** and **Page width** in pixels.

</td></tr><tr><td>

Page height \(in pixels\) \(Multilevel pivot report only\)

</td><td>

Shows when **Page size** is set to **Custom**. For non-standard paper sizes, multiply the page height in inches by 72 and enter the value in this field.

</td></tr><tr><td>

Page width \(in pixels\) \(Multilevel pivot report only\)

</td><td>

Shows when **Page size** is set to **Custom**. For non-standard paper sizes, multiply the page width in inches by 72 and enter the value in this field.

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

To edit the scheduled email of a report job, open the job from the Scheduled Jobs list. To stop scheduled emails of a report, delete the relevant job's row from the Scheduled Jobs list.

**Parent Topic:**[Create a scheduled job](../../time/task/t_CreateAScheduledJob.md)

**Related topics**  


[Advanced options for scheduled jobs](../../time/task/advanced-options-for-scheduled-jobs.md)

[Create a scheduled job](../../time/task/t_CreateAScheduledJob.md)

[Personalize the system date format](../../time/task/t_PersonalizeTheSystemDateFormat.md)

[Set a system time zone](../../time/task/t_SetASystemTimeZone.md)

