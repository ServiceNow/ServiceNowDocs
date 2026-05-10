---
title: Automatically run a script of your choosing
description: Schedule both conditional and non-conditional scripts. If Domain Separation is installed in the instance, you can also select, filter, sort, and schedule scripts based on their assigned domains.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Create a scheduled job, Scheduled jobs, System scheduler, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Automatically run a script of your choosing

Schedule both conditional and non-conditional scripts. If Domain Separation is installed in the instance, you can also select, filter, sort, and schedule scripts based on their assigned domains.

## Before you begin

Roles required: system\_scheduler\_admin

## About this task

The following is an example of a conditional script. It runs the scheduled job only if there are active incidents older than 30 days.

```
// Only run this Scheduled Job if there are active Incidents over 30 days old
var ga = new GlideAggregate('incident');
ga.addAggregate('COUNT');
ga.addQuery('active', 'true');
ga.addQuery('sys_created_on', '<', gs.daysAgo(30));
ga.query();
ga.next();
ga.getAggregate('COUNT') !== '0'
```

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select **New**.

3.  Select **Automatically run a script of your choosing**.

4.  On the form, fill in the fields.

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

Condition

</td><td>

A conditional script that determines if a scheduled job should run. The last expression of the script should evaluate to a Boolean \(true/false\) value. This text box appears only if you select **Use conditions**. **Warning:** Conditional scripts for scheduled report emails and Performance Analytics data collection jobs are executed in the sandbox. Therefore, function definitions are not allowed. Some API calls and keywords are also not allowed.For more information, see [Script sandbox evaluator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/script-sandbox.md).

After upgrade, jobs with conditional scripts that contain these disallowed API components finish with errors.

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

Run as \[Optional\]

</td><td>

Select another user to run the script execution as. Configure the form to add this field if it is not present.

</td></tr><tr><td>

Run this script

</td><td>

Name of the script to run at the scheduled date and time. For example, copy script logic from a business rule, or call a script include.

</td></tr></tbody>
</table>5.  If Domain Separation is installed in this instance, the following fields also appear for selecting, sorting, and scheduling jobs by domain.

    **Note:** The Domain Support - Domain Extensions Installer plugin installs these fields. To learn more, see [Request domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_ActivateDomainSeparation.md).

<table id="table_m2n_yyf_tlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain iterator

</td><td>

Check box that enables this job to run across multiple domains. If selected, the **Domain source table** and **Domain source filter** fields appear.

</td></tr><tr><td>

Domain source table

</td><td>

Name of the domain-separated table that is the source of the domains in which the scheduled job should run. For example, select **Department \(cmn\_department\)** if you want to use it as the source of the assigned domains used to schedule scripts. The scheduled job determines these domains from the sys\_domain field of the source table records. To learn more, see [Domain assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainAssignment.md). **Note:** It's a good idea to create a domain-separated table solely dedicated to sourcing domains, unless you have a use case that warrants using an existing one. If you do create a new one, simply select it using this field.

</td></tr><tr><td>

Domain source filter

</td><td>

Optional condition you can specify to filter the records queried from the selected domain source table. 1.  Select the field to use for filtering records.
2.  Add filtering conditions and operators to narrow the domain selection criteria. To learn more, see [Filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_Filters.md).


</td></tr></tbody>
</table>    The following processing takes place when scheduling a job in a domain-separated instance:

    -   It first queries the selected domain source table.
    -   If you specified a condition in the **Domain source filter** field, it applies the filtering condition to narrow down the resulting set of records.
    -   Finally, it retrieves its list of unique domains from the sys\_domain columns of these records.
6.  Select **Update** to update the scheduled job, **Execute Now** to execute the scheduled script immediately, or **Delete** to delete the job.


**Parent Topic:**[Create a scheduled job](../../time/task/t_CreateAScheduledJob.md)

**Related topics**  


[Advanced options for scheduled jobs](../../time/task/advanced-options-for-scheduled-jobs.md)

[Create a scheduled job](../../time/task/t_CreateAScheduledJob.md)

[Enable run types for scheduled job child tables](../../time/task/customize-run-times-for-scheduled-jobs.md#)

[Personalize the system date format](../../time/task/t_PersonalizeTheSystemDateFormat.md)

[Set a system time zone](../../time/task/t_SetASystemTimeZone.md)

[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

