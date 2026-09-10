---
title: Understand query patterns
description: Discover and identify performance issues with efficient query patterns to filter records, build dynamic queries, and optimize application performance across tables and modules within the ServiceNow instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-query-patterns-vid-tut.html
release: australia
topic_type: task
last_updated: "2026-02-12"
reading_time_minutes: 2
keywords: [query patterns, filtering records, dynamic queries, ServiceNow scripting, GlideRecord]
breadcrumb: [IO analytics, Monitor instance performance, Platform Health, Using Impact, Impact]
---

# Understand query patterns

Discover and identify performance issues with efficient query patterns to filter records, build dynamic queries, and optimize application performance across tables and modules within the ServiceNow instances.

## Before you begin

Role required: admin

## About this task

This query pattern model is a tool that is geared for discovering and identifying performance issues. It works best in below-an-hour range periods, ideally between 15 to an hour range, where you get better results around an event or a performance. So, it will pick up substantial performance issues and is useful in identifying the query pattern that is impacting the instance as a whole. The **Date Range** in this instance shows a Last 24-hour window:

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Monitor**.

2.  Log in to I**Instance Observer** and navigate to **Analytics** &gt; **Query Patterns**.

3.  Analyze and compare your query patterns.

    The **Summary** tab displays the pie charts:

    -   Top 20 by Total Volume
    -   Top 20 by Execution Time
    -   Top 20% increase in Total Execution Time compared to previous week
    \[Omitted image "io-query-pattern-sql.png"\] Alt text: Instance Observer query patterns.

    Top Transactions pull data from your instance's pattern tables to show you which operations are running most frequently and consuming the most time. Knowing your top transactions helps you identify what's normal for your instance and spot when something has changed. This module works best over longer time periods—a day or several days—but you can also use it for shorter periods when investigating specific performance events.

    Longer durations \(days or weeks\) show you trends over time. Shorter periods help when you're investigating a specific issue.

4.  Select the **Menu** list and select each of the options to view the details in the instance.

5.  Select the **Detailed** tab to display the breakdown details.

    Review the execution count, average execution time, and how these numbers fluctuated over your selected period. A large increase in count means users are running that transaction more. If average execution time is steady and fast \(milliseconds\), it's working as expected. Wide variations in execution time may indicate occasional slow runs caused by other factors.

    By default all URLs or labels are sorted by **Total Execution Time**. However, you can sort them by:

    -   Total Count
    -   Count Increase: Queries that have a high volume increase during that time frame.
    -   Total Execution Time Increase
    -   Average execution time
    -   Average execution time Increase
    -   First Sighted
    \[Omitted image "io-query-pattern-exe.png"\] Alt text: Detailed view of query patterns.

6.  Select the URL to view the **Avg Exe Time** and **Total Count** readings on the right pane.

7.  Select the **Transactions** list to view the **Active Transactions**, **Client Transactions**, **Background Transactions**, and **Slow Transactions**.

8.  Select the **Hash Code** link that takes you to the instance where you can view the slow queries model.


**Parent Topic:**[IO analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/io-analytics.md)

