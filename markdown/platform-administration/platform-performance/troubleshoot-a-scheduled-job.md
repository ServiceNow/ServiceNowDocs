---
title: Troubleshoot a scheduled job through Application Insights
description: Identify a scheduled job that is causing slow performance or running more often than necessary through the Scheduled Jobs table.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Troubleshoot a scheduled job through Application Insights

Identify a scheduled job that is causing slow performance or running more often than necessary through the Scheduled Jobs table.

## Before you begin

Role required: sn\_app\_insights.admin or admin

## Procedure

1.  Navigate to **All** &gt; **Application Insights** &gt; **Application Insights** &gt; **Scheduled Jobs**.

2.  Identify potential performance issues by viewing the executed script includes in the Scheduled Jobs table.

    -   Focus on a 1-day, 7-day, or 30-day period by selecting a day range.
    -   Identify long-running jobs by sorting on the **Average processing duration in range** column.
    -   Find out which jobs are running the most often by sorting on the **Run count in range** column.
    -   Identify jobs with the most errors by sorting on the **Error count in range** column.
3.  Investigate a potential issue by selecting a scheduled job.

    The **Processing Duration** detail graph shows the scheduled job's average execution time and its 1-day moving average.

4.  View the performance for the scheduled job over time by analyzing the **Processing Duration** detail graph.

    ![Processing duration detail graph](../image/app-insights-scheduled-jobs.png)

    Determine whether the job is running unexpectedly, running during business hours, or running during peak usage time periods.

5.  View the job's details and schedule to determine what improvements you can make by selecting **View Record**.

    -   Change the job's schedule if the job is running too often or during times of peak usage.
    -   Determine the best time to run a scheduled job by looking for periods of low user activity on the **Logged in Users** graph on the **Session Info** tab.
    -   Review the scheduled script or report and determine whether it can be optimized or removed.
6.  Select **Update**.

7.  Check the performance of the scheduled job over time by viewing the **Processing Duration** detail graph.

8.  Continue making adjustments to the schedule or job details until the average processing duration improves.


**Parent Topic:**[Application Insights](../concept/application-insights.md)

