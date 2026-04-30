---
title: Schedule data collection for a Platform Analytics Solution
description: Enable the periodic data collection job for your Platform Analytics Solution. Check that the time that it runs is correct.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Collect data for Platform Analytics Solutions, Analytics solutions, Platform Analytics]
---

# Schedule data collection for a Platform Analytics Solution

Enable the periodic data collection job for your Platform Analytics Solution. Check that the time that it runs is correct.

Prerequisites
:   [Run historical data collection for a Platform Analytics Solution](historical-data-nowintel-solution.md)

## Before you begin

Role required: pa\_admin, admin

## About this task

Every Platform Analytics Solution includes a periodic [data collection job](../concept/performance-analytics-glossary.md#).

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.

2.  Filter the job list on \[\[\[Run\]\[is not one of\]\[Once \| On Demand\]\] AND \[\[Active\]\[is\]\[false\]\]\].

    You now see only periodic data collection jobs that you have not activated.

3.  Open the periodic data collection job for your Platform Analytics Solution.

    The following steps refer to the Job Parameters section of the job record.

    ![Active checkbox on scheduled job record](../image/nowintel-solution-active-job.png)

4.  Ensure that the user specified in the **Run as** field exists.

    If you are using domain separation, you collect records only from domains that the **Run as** user can view. However, the access control list permissions of the **Run as** user do not affect data collection.

5.  Verify that the **Run As tz** time zone is appropriate for your company.

    The database queries created for this job use this time zone, which is reflected in the logs for this job. This time zone also determines what day is "Today" for indicator conditions like \[\[Created\]\[on\]\[Today\]\].

6.  Select **Active** to enable the scheduled run of the job.

    Scheduling options are now available.

7.  Ensure that the time that the job runs is during your company downtime.

    -   The **Time** value is based on the time zone for your user session, not the **Run as tz** time zone.
    -   To get an accurate measurement for a day, the day must have completed. For a Daily job, the **Time** value should be between midnight and 06:00 in the **Run as tz** time zone, to collect for the previous day. For example, if you are logged in from New York and want to run the job at 05:00 in the System/Los Angeles time zone, set **Time** to 08:00:00.
    -   For a Monthly job, you also set the day that you want to run the job on. Generally set it to run on the first day of the month, soon after midnight in the **Run as tz** time zone. This setting gets all the data for the preceding month, regardless of the length of the month.

## Result

After the next collection period, the dashboards and widgets should show scores from that period.

## What to do next

Check the **Job Logs** to see if the job ran successfully after the next period.

**Parent Topic:**[Collect data for Platform Analytics Solutions](../concept/collect-data-nowintel-solutions.md)

**Previous topic:**[Run historical data collection for a Platform Analytics Solution](historical-data-nowintel-solution.md)

**Next topic:**[User Experience Analytics](../../../administer/user-exp-analytics/content-framework/landing-page/user-exp-analytics-landing.md)

**Related topics**  


[Create or schedule a data collection job](t_CreatASchedDataCollJob.md)

