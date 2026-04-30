---
title: AI Search analytics dashboard
description: The AI Search analytics dashboard displays key performance metrics, trends, and reports for AI Search usage. Analysts can apply interactive filters to view performance analytics for individual search applications and to select the time frame to analyze.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-27"
reading_time_minutes: 6
breadcrumb: [Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# AI Search analytics dashboard

The AI Search analytics dashboard displays key performance metrics, trends, and reports for AI Search usage. Analysts can apply interactive filters to view performance analytics for individual search applications and to select the time frame to analyze.

To access the AI Search analytics dashboard, navigate to **All** &gt; **User Experience Analytics**, select an application's **Launch Dashboard** link, then select the Search Analytics icon ![](../image/icon-appsee-ai-srch-analytics.png) or link in the modules menu. To learn more about the User Experience Analytics dashboard, see [Overview of the dashboard](https://www.servicenow.com/docs/access?context=user-exp-analytics-dashboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

**Note:** If the dashboard doesn't load, follow the steps from [Configure Service Portal to send analytics data](adv-ais-enable-sp-analytics-data.md) to enable it.

In the **Queries** section of the dashboard, you can view the query lists on their own page by selecting **View all**. To return to the main dashboard from the sub-page, select **AI Search Analytics**.

You can improve the visual experience by using the dark theme. For more information, see [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

## Required ServiceNow AI Platform roles

To view the AI Search analytics dashboard, you must have the ais\_admin role and one of the following roles:

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

Specifies the search application configuration for which you want to see search analytics metrics, trends, and reports. You can search for a search application configuration or select its name in the list. Select **Apply** to make your filter selection take effect.**Note:** You can only select a single search application configuration in this filter.

The filter list includes search application configurations that are configured to use AI Search and that are used in any of the following contexts:

-   A service portal
-   A Next Experience workspace search
-   Next Experience global search
-   Mobile Platform search
-   Now Assist in Virtual Agent enhanced chat
-   Recommended Actions

The dashboard reports metrics for all search queries in the selected search application configuration that satisfy your **Date range** constraint. These may include user searches submitted directly to a search application that uses the configuration and searches submitted through interaction with other ServiceNow AI Platform features, such as Virtual Agent.

</td></tr><tr><td>

Date range

</td><td>

Specifies the range of dates for which you want to see search analytics metrics, trends, and reports. By default, the dashboard displays data from the last 30 days. You can choose one of the preset date ranges or set your own start and end dates. Select **Apply** to make your filter selection take effect. The dashboard retains data from the last 180 days. If you select a date from outside of this range, the system displays an error message and the dashboard reverts to the last valid date range selection. If you haven't selected any valid date range, the dashboard reverts to its default date range.

**Note:** When you select a custom date range, the dashboard may take longer to load than when you select a preset date range.

The dashboard reports metrics for all search queries in the selected date range that satisfy your **Search application** constraint. These may include user searches submitted directly to the search application and searches submitted through interaction with other ServiceNow AI Platform features, such as Virtual Agent.

</td></tr></tbody>
</table>## Metrics, trends, and reports

The dashboard includes a main page and a Queries sub-page accessible from the **View all** link in the **Queries** section. The **View all** link in the **Search queries** section opens the Search Events \[sys\_search\_event\] table in list view.

**Note:** To improve performance, the AI Search analytics dashboard caches results from its source tables for 60 minutes. As a result, you may not see search queries from the last 60 minutes reflected in the dashboard's metrics, trends, and visualizations.

<table id="table_byh_gk5_1hc"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search users

</td><td>

This numeric metric shows the total number of unique users who submitted search queries.The trend describes how the number of unique search users has changed since the start of your selected date range.

The chart shows the number of unique search users for dates in your selected date range.

![Search users metric, trend, and chart.](../image/ai-search-analytics-dashboard-search-users.png)**Note:** Searches performed while impersonating another user are ignored for this metric, trend, and chart.

</td></tr><tr><td>

Total queries

</td><td>

This numeric metric shows the total number of search queries submitted.The trend describes how the number of search queries has changed since the start of your selected date range.

The chart shows the number of search queries submitted for dates in your selected date range.

![Total queries metric, trend, and chart.](../image/ai-search-analytics-dashboard-total-queries.png)

</td></tr><tr><td>

Searches over time

</td><td>

This chart shows counts for searches in your selected date range. It includes three sets of values:1.  The number of search queries executed
2.  The number of search results that users clicked \(selected\)
3.  The number of Genius Result answers that users clicked \(selected\)

![Searches over time chart.](../image/ai-search-analytics-dashboard-searches-over-time.png)

</td></tr><tr><td>

Average response time

</td><td>

This numeric metric shows the average response time for search queries in milliseconds.The chart shows the distribution of search query response times, broken out into buckets.

The trend describes how the average response time for search queries has changed since the start of your selected date range.

![Average response time metric, chart, and trend.](../image/ai-search-analytics-dashboard-avg-response-time.png)

</td></tr><tr><td>

Average click position

</td><td>

This numeric metric indicates the average position of user-selected search query results.The chart shows the distribution of positions for user selected search query results.

The trend describes how the average click position has changed since the start of your selected date range.

![Average click position metric, chart, and trend.](../image/ai-search-analytics-dashboard-avg-click-position.png)

</td></tr><tr><td>

Self-Solved Rate

</td><td>

This metric indicates the percentage of search queries that produced a search result click \(selection\).The chart shows the distribution of search queries that did and didn't produce search result clicks.

The trend describes how the self-solved rate has changed since the start of your selected date range.

![Self-solve rate metric, chart, and trend.](../image/ai-search-analytics-dashboard-self-solve-rate.png)

</td></tr></tbody>
</table><table id="table_uyh_gk5_1hc"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search queries

</td><td>

This list shows user-submitted search queries.Each entry displays the following details:

-   **Search query**: The search query.
-   **Click position**: The result number for the first search result the user selected, or 0 if the user didn't select any search result.
-   **Genius Result type**: The Genius Result configuration that generated the first Genius Result answer for the search query, or **N/A** if no Genius Result answer was displayed for the search query.
-   **Language**: The language in which the search query was submitted.
-   **Geography**: The geographical region associated with the user who submitted the search query.
-   **Organization**: The organization that the user who submitted the search query belongs to.
-   **Date**: The date the search query was executed.

To view entries for these search queries in the Search Events \[sys\_search\_event\] table, select **View all**.

![Search queries list.](../image/ai-search-analytics-dashboard-search-queries.png)

</td></tr></tbody>
</table><table id="table_xl5_nr5_1hc"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Top queries

</td><td>

This list shows the most frequently submitted search queries.![Top queries list.](../image/ai-search-analytics-dashboard-top-query-themes.png)

To view this list on its own sub-page, select **View all**. To return to the main dashboard from the sub-page, select **AI Search Analytics**.

</td></tr><tr><td>

Queries with no clicks

</td><td>

This list shows the most frequently submitted search queries for which users didn't select any search result.![Queries with no clicks list.](../image/ai-search-analytics-dashboard-queries-zero-clicks-themes.png)

To view this list on its own sub-page, select **View all**. To return to the main dashboard from the sub-page, select **AI Search Analytics**.

</td></tr><tr><td>

Queries with no results

</td><td>

This list shows the most frequently submitted search queries that produced no results. ![Queries with no results list.](../image/ai-search-analytics-dashboard-queries-no-results-themes.png)

To view this list on its own sub-page, select **View all**. To return to the main dashboard from the sub-page, select **AI Search Analytics**.

</td></tr></tbody>
</table><table id="table_pn2_4hq_chc"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Top clicked results

</td><td>

This list shows the most frequently clicked search results.![Top clicked results list.](../image/ai-search-analytics-dashboard-top-clicked-results.png)

</td></tr></tbody>
</table>