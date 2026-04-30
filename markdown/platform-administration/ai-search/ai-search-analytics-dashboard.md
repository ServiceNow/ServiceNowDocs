---
title: AI Search Analytics dashboard
description: The AI Search Analytics dashboard displays key performance metrics, trends, and reports for AI Search usage on its main page. Its Queries page displays additional information on search queries. Interactive filters enable analysts to view performance analytics for individual search applications over the last 180 days and to select the time frame to analyze.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-19"
reading_time_minutes: 8
breadcrumb: [Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Analytics dashboard

The AI Search Analytics dashboard displays key performance metrics, trends, and reports for AI Search usage on its main page. Its Queries page displays additional information on search queries. Interactive filters enable analysts to view performance analytics for individual search applications over the last 180 days and to select the time frame to analyze.

![AI Search Analytics dashboard - main page, Overview section.](../image/ais-analytics-db-1-overview.png "AI Search Analytics dashboard - main page, Overview section")

![AI Search Analytics dashboard - main page, Search results section.](../image/ais-analytics-db-2-srch-results.png "AI Search Analytics dashboard - main page, Search results section")

![AI Search Analytics dashboard - main page, Queries section.](../image/ais-analytics-db-3-queries.png "AI Search Analytics dashboard - main page, Queries section")

![AI Search Analytics dashboard - main page, Top clicked results section.](../image/ais-analytics-db-4-top-results.png "AI Search Analytics dashboard - main page, Top clicked results section")

![AI Search Analytics dashboard - Queries page, Queries over time report.](../image/ais-queries-dashboard-1.png "AI Search Analytics dashboard - Queries page, Queries over time report")

![AI Search Analytics dashboard - Queries page, Query Analysis section.](../image/ais-queries-dashboard-2.png "AI Search Analytics dashboard - Queries page, Query Analysis section")

To access the AI Search Analytics dashboard, navigate to **All** &gt; **User Experience Analytics**, select an application's **Launch Dashboard** link, then select the Search Analytics icon ![](../image/icon-appsee-ai-srch-analytics.png) or link in the modules menu. To learn more about the User Experience Analytics dashboard, see [Overview of the dashboard](https://www.servicenow.com/docs/access?context=user-exp-analytics-dashboard&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

**Note:** If the dashboard doesn't load, follow the steps from [Configure Service Portal to send analytics data](adv-ais-enable-sp-analytics-data.md) to enable it.

To access the Queries page, select **View all** in the **Queries** section header of the main page.

You can improve the visual experience by using the dark theme. For more information, see [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Required ServiceNow AI Platform roles

To view the AI Search Analytics dashboard, you must have the ais\_admin role and one of the following roles:

-   analytics\_admin
-   analytics\_viewer
-   portal\_analytics\_admin
-   portal\_analytics\_viewer
-   web\_analytics\_admin
-   web\_analytics\_viewer

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_ov2_tj4_2fb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Any of the following:-   Portal Analytics administrator or viewer
-   User Experience Analytics administrator or viewer
-   Web Analytics administrator or viewer

</td><td>

-   View and monitor search usage and search performance for a specified search application and date range
-   Review search trends to better understand the needs of search application end users
-   Gain insights on how to improve search experience and knowledge coverage by identifying common search queries that yield no results or low-quality results

</td></tr></tbody>
</table>## Interactive filters

<table id="table_bh4_32x_3pb"><thead><tr><th>

Filter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search application

</td><td>

Specifies the search application for which you want to see search analytics metrics, trends, and reports. You can search for a search application or select its name in the list. Select **Apply** to make your filter selection take effect.

**Note:** You can only select a single search application in this filter.

 The filter list includes search applications that are configured to use AI Search and that are used in any of the following contexts:

-   A service portal
-   A Next Experience workspace search
-   Next Experience global search
-   Mobile Platform search

 The dashboard reports metrics for all search queries in the selected search application that satisfy your **Date range** constraint. These may include user searches submitted directly to the search application and searches submitted through interaction with other ServiceNow AI Platform features, such as Virtual Agent.

</td></tr><tr><td>

Date range

</td><td>

Specifies the range of dates for which you want to see search analytics metrics, trends, and reports. By default, the dashboard displays data from the last 30 days. You can choose one of the preset date ranges or set your own start and end dates. Select **Apply** to make your filter selection take effect.

 The dashboard retains data from the last 180 days. If you select a date from outside of this range, the system displays an error message and the dashboard reverts to the last valid date range selection. If you haven't selected any valid date range, the dashboard reverts to its default date range.

**Note:** When you select a custom date range, the dashboard may take longer to load than when you select a preset date range.

 The dashboard reports metrics for all search queries in the selected date range that satisfy your **Search application** constraint. These may include user searches submitted directly to the search application and searches submitted through interaction with other ServiceNow AI Platform features, such as Virtual Agent.

</td></tr></tbody>
</table>## Metrics, trends, and reports

The dashboard includes a main page and a Queries page accessible from the **View all** link in the **Queries** section.

**Note:** To improve performance, the AI Search Analytics dashboard caches results from its source tables for 60 seconds. You may not see search queries from the last 60 seconds reflected in the dashboard's metrics, trends, and visualizations.

<table id="table_ekb_hgw_w4b"><thead><tr><th>

Title

</th><th>

Visualization type

</th><th>

Source tables

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="4">

Overview section

</td></tr><tr><td>

Search users

</td><td>

Line ![](../../performance-analytics/image/line-icon.png)

</td><td>

-   Metric and trend: AI Search Analytics Dashboard Unique Search Users \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_unique\_search\_users\]
-   Report: AI Search Analytics Dashboard Daily Search Users \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_daily\_search\_users\]

</td><td>

-   Metric indicates the total count of unique users who submitted search queries in the selected application and date range.
-   Trend describes how the number of unique search users changed in the selected application and date range.
-   Report displays the number of unique search users in the selected application for dates in the selected range.

 **Note:** Searches performed while impersonating another user are ignored for this metric, trend, and report.

</td></tr><tr><td>

Total queries

</td><td>

Line ![](../../performance-analytics/image/line-icon.png)

</td><td>

AI Search Analytics Dashboard Total Searches and Clicks by Date \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_total\_searches\_by\_date\]

</td><td>

-   Metric indicates the total count of search queries submitted in the selected application and date range.
-   Trend describes how the count of search queries submitted changed in the selected application and date range.
-   Report displays the count of search queries submitted in the selected application for dates in the selected range.

</td></tr><tr><td>

Average response time

</td><td>

Donut ![](../../performance-analytics/image/donut-icon.png)

</td><td>

-   Metric and trend: AI Search Analytics Dashboard Average Search Response Time \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_average\_response\_time\]
-   Report: AI Search Analytics Dashboard Daily Average Response Time \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_daily\_average\_response\_time\]

</td><td>

-   Metric indicates the average search query response time for the selected application and date range.
-   Trend describes how the average search query response time changed in the selected application and date range.
-   Report displays the distribution of search query response times in the selected application for dates in the selected range.Response times are categorized as &lt;1 second, 1–2 seconds, or &gt;2 seconds.

</td></tr><tr><td class="sub-head" colspan="4">

Searches over time section

</td></tr><tr><td>

Searches over time

</td><td>

Line ![](../../performance-analytics/image/line-icon.png)

</td><td>

AI Search Analytics Dashboard Total Searches and Clicks by Date \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_total\_searches\_by\_date\]

</td><td>

The count of search queries executed, search result clicks, and Genius Result clicks in the selected application for dates in the selected range.

</td></tr><tr><td class="sub-head" colspan="4">

Search results section

</td></tr><tr><td>

Genius Results \(triggered vs. clicked\)

</td><td>

Horizontal Bar ![](../../performance-analytics/image/horizontal-bar.png)

</td><td>

AI Search Analytics Dashboard Trending Genius Result \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_trending\_genius\_result\]

</td><td>

The most frequently triggered and selected Genius Result configurations in the selected application and date range.

</td></tr><tr><td>

Average click position

</td><td>

Donut ![](../../performance-analytics/image/donut-icon.png)

</td><td>

AI Search Analytics Dashboard Average Click Position \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_average\_click\_position\]

</td><td>

-   Metric indicates the average position of user-selected search query results for the selected application and date range.

**Note:** Positions indicate result numbers. For example, a position of 2 means that the user selected the second result returned for a search query.

-   Trend describes how the average position of user-selected search query results changed in the selected application and date range.
-   Report displays the distribution of positions for user-selected search query results in the selected application for dates in the selected range.

</td></tr><tr><td>

Self-Solved Rate

</td><td>

Line ![](../../performance-analytics/image/line-icon.png)

</td><td>

AI Search Analytics Dashboard Total Searches and Clicks by Date \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_total\_searches\_by\_date\]

</td><td>

-   Metric indicates the percentage of search queries that produced a search result click for the selected application and date range.
-   Trend indicates how the percentage of search queries that produced a search result click changed in the selected application and date range.
-   Report indicates the percentage of search queries that produced a search result click in the selected application for dates in the selected range.

</td></tr><tr><td class="sub-head" colspan="4">

Queries section

</td></tr><tr><td>

Top queries

</td><td>

Table ![](../image/table-icon.png)

</td><td>

AI Search Analytics Dashboard Trending Search Terms \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_trending\_search\_terms\]

</td><td>

The most frequently submitted search queries in the selected application and date range, by percentage of total search queries for the application and date range.

 To access the Queries dashboard and see more details and entries for this report, select **View all** in the **Queries** section header.

</td></tr><tr><td>

Queries with no clicks

</td><td>

Table ![](../image/table-icon.png)

</td><td>

AI Search Analytics Dashboard Queries with no Clicks \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_queries\_with\_no\_clicks\]

</td><td>

The most frequently submitted search queries in the selected application and date range for which users didn't select any search result, by count.

 To access the Queries dashboard and see more details and entries for this report, select **View all** in the **Queries** section header.

</td></tr><tr><td>

Queries with no results

</td><td>

Table ![](../image/table-icon.png)

</td><td>

AI Search Analytics Dashboard Queries with no Results \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_queries\_with\_no\_results\]

</td><td>

The most frequently submitted search queries in the selected application and date range that produced no results, by count.

 To access the Queries dashboard and see more details and entries for this report, select **View all** in the **Queries** section header.

</td></tr><tr><td class="sub-head" colspan="4">

Top clicked results section

</td></tr><tr><td>

Top clicked results

</td><td>

Table ![](../image/table-icon.png)

</td><td>

AI Search Analytics Dashboard Trending Search Content \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_trending\_search\_content\]

</td><td>

The most frequently clicked search results in the application and date range, by percentage of views that resulted in a click.

</td></tr></tbody>
</table><table id="table_jtb_g1h_dqb"><thead><tr><th>

Title

</th><th>

Report type

</th><th>

Source tables

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Queries over time

</td><td>

Line ![](../../performance-analytics/image/line-icon.png)

</td><td>

AI Search Analytics Dashboard Total Searches and Clicks by Date \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_total\_searches\_by\_date\]

</td><td>

The count of search queries executed in the selected application for dates in the selected range.

</td></tr><tr><td class="sub-head" colspan="4">

Query Analysis section

</td></tr><tr><td>

Top queries

</td><td>

Table ![](../image/table-icon.png)

</td><td>

AI Search Analytics Dashboard Trending Search Terms \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_trending\_search\_terms\]

</td><td>

The most frequently submitted search queries in the selected application and date range, by percentage of total search queries for the application and date range.

 To view additional details on a search query, including its average response time and top results, select the query entry in the Top queries column.

 To display additional report entries, select **Load More** at the bottom of the table.

</td></tr><tr><td>

Queries with no clicks

</td><td>

Table ![](../image/table-icon.png)

</td><td>

AI Search Analytics Dashboard Queries with no Clicks \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_queries\_with\_no\_clicks\]

</td><td>

The most frequently submitted search queries in the selected application and date range for which users didn't select any search result, by count.

 To display additional report entries, select **Load More** at the bottom of the table.

</td></tr><tr><td>

Queries with no results

</td><td>

Table ![](../image/table-icon.png)

</td><td>

AI Search Analytics Dashboard Queries with no Results \[sn\_ais\_admin\_tools\_ai\_search\_analytics\_dashboard\_queries\_with\_no\_results\]

</td><td>

The most frequently submitted search queries in the selected application and date range that produced no results, by count.

 To display additional report entries, select **Load More** at the bottom of the table.

</td></tr></tbody>
</table>