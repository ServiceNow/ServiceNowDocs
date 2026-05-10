---
title: Create or schedule a data collection job
description: Schedule a data collection job to regularly collect Performance Analytics indicator scores and snapshots.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Collecting indicator scores, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create or schedule a data collection job

Schedule a data collection job to regularly collect Performance Analytics indicator scores and snapshots.

## Before you begin

Before defining data collection jobs, make sure that indicator sources, breakdown sources, and indicators have been defined. Otherwise, jobs cannot return any results.

Roles required: pa\_data\_collector or admin

## About this task

The important items to know when you configure a data collection job are:

-   Collection period
-   Collection timezone
-   Collected scores domain, if domains are used.
-   The collection job runs without any restrictions. It does not use the permissions of the user who runs it.

Data collection jobs run different steps to collect scores and to collect text analytics data. By default, jobs collect both types of data. To improve performance, you can instead schedule separate jobs for scores and for text analytics data.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs** and click **New**.

    You can instead edit an existing data collection job, for example to change the schedule of when the job runs. In this case, navigate to **Performance Analytics** &gt; **Data Collector** &gt; **Jobs** and click the job name.

2.  In the **Name** field, give the job a meaningful name.

    Follow a standard format for naming data collector jobs, such as \[PA Indicator\] Daily Data Collection, \[PA Indicator\] Historic Data Collection...

3.  In the **Operator** field, select whether to collect data for an absolute or a relative time period.

    |Operator value|Description|
    |--------------|-----------|
    |**Fixed**|Collects data for an absolute time period.|
    |**Relative**|Collect data for a period of time that is relative to the time when the job is run.|

4.  If you selected **Fixed** as the operator, select the **Fixed start** date and the **Fixed end** date.

5.  If you selected **Relative** as the operator, specify the intervals prior to the run time to collect data from.

    1.  In the fields **Relative start** and **Relative start interval**, set the number and the length, respectively, of time periods in the past to begin to collect data from.

    2.  In the fields **Relative end** and **Relative end interval**, set the number and the length, respectively, of the last period in the past to collect data from.

        **Tip:**

        -   Most indicators, and therefore most data collection jobs, run Daily. Daily scheduled jobs normally should collect for the most recently completed day. Therefore, they should have both a relative start and relative end of one day ago. Run historical data collection jobs, which have longer collection periods, only once.
        -   If you plan to use this job with indicators that use business calendars, consider the **periods ago** interval. This interval is based on the periods that are defined for a business calendar.
        For example, you want to collect scores for a set of several new indicators with a daily frequency, all using the same indicator source. First you create a historical data collection job that collects data from two months ago up to the day before yesterday. For this job, enter **60** in **Relative start** and **days ago** in **Relative start interval**. Enter **2** in **Relative end** and **days ago** in **Relative end interval**. Set the **Run** field to **On Demand**. Click **Execute now** and run this job once, to collect the initial scores.

        Create a second job with relative start and end of 1 day ago and set the **Run** field to **Daily**. Activate this job to collect the scores for yesterday and all future scores for the day before the job is run.

6.  Fill in the **Job parameters**, as appropriate.

<table id="tbl_PerformanceAnalyticsDataCollectionJobProperties"><thead><tr><th>

Job parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run as

</td><td>

For domain separated instances, select the user that runs this job. The job collects scores from facts table and Performance Analytics records that have either the Global domain or are in the domain of this user. The data collection job follows only the domain, not the permissions of this user. ACLs and business rules do not apply to data collection jobs. Any user can run the job.

 **Important:** If you select a domain configuration for this job, it overrides the **Run as** user. See Step [9](t_CreatASchedDataCollJob.md#step_domain-config) in this topic.

</td></tr><tr><td>

Run as tz

</td><td>

Select the time zone that the queries use when they are executed from the job. Use the reporting time zone of your company if one exists. By default the System time zone is used. This time zone determines what day is "Today" for conditions like \[\[Opened\]\[on\]\[Today\]\].

</td></tr><tr><td>

Active

</td><td>

If selected, as it is by default, the data collection occurs at the scheduled date and time.

</td></tr><tr><td>

Run

</td><td>

Select the schedule for collecting the data. Choices are: -   Daily
-   Weekly
-   Monthly
-   Periodically
-   Once
-   On demand
 If you are using business calendars, you also have these options, for the start and end of the business calendar period \(See [Define business calendar entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/define-business-calendar-entries.md)\):

-   Business calendar: Entry start
-   Business calendar: Entry end
 If you are creating a historical data collection job, schedule the job to run On demand.

</td></tr><tr><td>

Day

</td><td>

-   If **Run** is **Weekly**, specify the day of the week.
-   If **Run** is **Monthly**, specify the day of the month.
 To collect at the end of the month, set for day 1 and set **Time** to soon after midnight. This setting collects data for a completed month regardless of the length of the month.

</td></tr><tr><td>

Repeat Interval

</td><td>

If **Run** is **Periodically**, specify the amount of time between scheduled data collections, in days and hour.

</td></tr><tr><td>

Starting

</td><td>

If **Run** is **Periodically** or **Once**, specify the date and time of the first scheduled data collection.

</td></tr><tr><td>

Time

</td><td>

Time that the job runs, on 24 hour clock. Field appears after **Active** is selected.-   Time based on the time zone for your user session, not the **Run as tz** time zone.
-   Generally set for an hour between midnight and 6 am at your company, to collect the last complete period.
 For example, if you are in New York and want to collect data at 5 am for your company that is on Los Angeles time, set the time to 08:00:00.

</td></tr><tr><td>

Collect

</td><td>

Data collection jobs have separate steps for collecting scores and for collecting text analytics. Select one of:-   Scores only
-   Text index only
-   Both scores and text index \(default\)
 For more information, see [Set up text analytics](set-up-text-analytics.md).

</td></tr><tr><td>

Conditional

</td><td>

If checked, the data collection occurs only if certain conditions are met.

</td></tr><tr><td>

Conditions

</td><td>

A conditional script that determines if a scheduled job should run. The last expression of the script should evaluate to a Boolean \(true/false\) value. This text box appears only if you select **Use conditions**. **Warning:** Conditional scripts for Performance Analytics data collection jobs are executed in the sandbox. Therefore, function definitions are not allowed. Some API calls and keywords are also not allowed. For more information, see Script sandbox property.

After upgrade, jobs with conditional scripts that contain these disallowed API components will conclude with "Collected with errors." These jobs do not collect scores.

The `com.snc.pa.dc.script.use.sandbox` system property controls whether data collection scripts use the sandbox. Only users with the security\_admin role can modify this property. Exercise caution when turning off this property. When set to false, unauthorized users may be able to execute malicious actions on your instance.

</td></tr></tbody>
</table>7.  Right-click the form header and select **Save**.

8.  In the **Indicators** related list, click **Edit** and select the indicators that this job collects data for.

    **Important:**

    -   Include at least one indicator for the job. Otherwise, the job cannot return any results.
    -   To help keep jobs maintainable, try not to associate an indicator with more than one active collection job unless you have a clear use case. If you are trying to get real-time data, consider using a real-time indicator.
    -   The data collection job produces one database query for each indicator source for the associated indicators. Thus the data for all indicators that share an indicator source represent the same point in time.
9.  If you have enabled domain configurations, you can select a domain configuration to associate with this job in the **Domain configurations** related list.

    Domain configurations are grouping of domains based on their visibility to a user group or other condition. These groupings can include parent-child relationships. If you select a domain configuration for a job, the job collects scores for records in the domains of the configuration, including the global domain. Domain configurations override the **Run as** user. For more information, see [Grouping domains in Performance Analytics domain configurations](../concept/pa-domain-separation-msp.md).

10. Click **Submit**.


## What to do next

-   By default, for each job indicator, data is collected for all breakdowns and the indicator itself. To change this configuration for an indicator, see [Configure a job indicator](configure-job-indicator.md).
-   If you have enabled domain support, you have a related list named **Domain configuration**. In this tab, click **Edit** to relate an existing domain configuration with this job or click **New** to create a new domain configuration. For more information, see [Create a domain configuration](create-domain-configuration.md).

**Parent Topic:**[Collecting indicator scores](../concept/c_ClctData.md)

