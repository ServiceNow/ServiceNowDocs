---
title: Instance Observer reports overview
description: Reports in Instance Observer offer insights into the health of the instances, tracks database growth, and encryption status. The reports help you to analyze trends, and to schedule, download, and share these reports.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-17"
reading_time_minutes: 4
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Instance Observer, Platform Health, Using Impact, Impact]
---

# Instance Observer reports overview

Reports in Instance Observer offer insights into the health of the instances, tracks database growth, and encryption status. The reports help you to analyze trends, and to schedule, download, and share these reports.

## Daily Performance Metric Report

-   **ServiceNow Platform Health**
    -   **Standby Lag Anomaly**

        Indicates a delay in replication to the database that resides in the standby datacenter, and this results in delays if an AHA was required.

        ServiceNow has an internal monitor and standard operating procedures when lag to the standby site is present. If ServiceNow determines a risk or impact due to lag, a P2 case will be opened automatically.

        **Note:** Not all breach will result in a case. For sub-prod instances, ignore this field in the report.

    -   **Server Response Time Anomaly**

        Indicates that user transactions were most likely impacted.

        To determine what transaction\(s\) was the cause use the transaction logs with a filter +/- 5 minutes around the time of impact.

        **Note:** See the [Using the transaction logs \[KB0584420\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0584420) article in the Now Support Knowledge Base

    -   **Database Response Time Anomaly**

        Indicates that the database is impacted with a very strong collection to user impact.

        See the [Targeting query patterns to maintain or improve performance \[KB1064766\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1064766) article in the Now Support Knowledge Base for the steps and then adjust the time range to +/- 15 minutes around the time of the breach.

-   **Health Indicator**
    -   **Today’s count and yesterday’s count**

        Provides a quick glimpse of key health indicators for today and yesterday.

        -   Slow Transaction Count is calculated based on any transactions that ran for more than 4.5 seconds.
        -   Slow Queries Count is calculated based on any queries that ran for more than 1 second.
        -   Long-running jobs Count is calculated based on any job that ran for more than 60 minutes.
        An indicator trend is displayed if the counts are going excessively higher as compared from the 30-day average.

    -   **30-day average**

        Provides a quick glimpse of key health indicators for the last 30-days.

        -   Slow Transaction Count Average is calculated based on any transactions that ran for more than 4.5 seconds per day averaged over 30 days.
        -   Slow Queries Count Average is calculated based on any queries that ran for more than 1 second per day averaged over 30-days
        -   Long running jobs Count Average is calculated based on any jobs that ran for more than 60 minutes day averaged over 30-days
    -   **Top 10 slow transactions**

        Provides a quick glance at your most sluggish 10 transactions.

        The report presents a top 10 list by first identifying the top 50 mostly executed transactions on this instance based on total execution time. Among the 50 transactions list it reports the top 10 transactions by the average execution time.

    -   **Top 10 slow queries**

        Provides a quick glance at your most sluggish 10 queries.

        The report comes up with this top 10 list by first identifying the top 50 mostly executed queries on this instance by total execution time. Among those 50 queries, it reports the top 10 queries by the average execution time.

    -   **Top 10 running jobs**

        Provides a glance at the most sluggish 10 jobs by execution time per node by worker.

    -   **Critical support cases**

        Provides a quick glance at your active cases \(P1 and P2\) created within the past 30 days.


## Performance Trend Report

This report provides users with the ability to quickly combine various performance metrics into a single comprehensive report. The report also calculates the trend between the selected time period and the comparison to the previous time period. Since the data is available only for 6 months, if the time period of the report is selected beyond 3 months, the report does not calculate the trend.

**Note:** The Standby Lag option should not be selected for sub-prod instances.

## Database Growth Report

This report provides users with the ability to create a report on the database growth.

**Note:** If shards are not configured, then the chart for database size will not display any shards database. The table growth is sorted in descending order by the highest table size.

For more information on reports, see [Instance performance telemetry reports](instance-observer-reporting.md).

## URL for graphs

-   You can share the URL for charts with respective timestamp so you can open the link directly in a browser with the selected options.
-   You can share the URL at the Performance, Availability, Triage, Reports, and Configure Notification under **Alerts** tab.
-   IO is supported on Google Chrome and Mozilla Firefox and the links are valid on these browsers. You must log in to the respective browser to view the shared URL.
-   There is a limitation with sharing the URL for Triage — both the sender and recipient must have the same instance enabled in their accounts.

**Parent Topic:**[Overview of Instance Observer metrics](../concept/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Data Replication](instance-observer-metrics.md)

[Anomaly insights](addl-inf-io-anomaly.md)

[Feature availability based on package](io-feature-availability.md)

