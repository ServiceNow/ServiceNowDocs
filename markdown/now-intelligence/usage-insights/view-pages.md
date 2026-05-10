---
title: Usage Insights for pages and screens
description: The Pages module for UI Analysis in Usage Insights shows analytics specific to pages on the web-based UI in terms of page use and navigation. View user action, performance, and navigation details for each web page to identify pages where users might be having issues and optimize workflows accordingly.See user actions, performance and navigation analytics for each page.
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Usage Insights, Usage Insights, Platform Analytics]
---

# Usage Insights for pages and screens

The Pages module for UI Analysis in Usage Insights shows analytics specific to pages on the web-based UI in terms of page use and navigation. View user action, performance, and navigation details for each web page to identify pages where users might be having issues and optimize workflows accordingly.

The analogous module for mobile applications is Screens. For more information, see [Usage Insights for mobile applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-analytics.md).

![UXA Web Page details page with data visualizations for sessions, views, and durations and bar visualizations of preceding and succeeding pages](../image/uxa-web-page-details2.png)

<table id="table_zxj_x2s_gwb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Page stats**

</td></tr><tr><td>

Sessions

</td><td>

Shows the number of sessions contained on the specified page. If a page was opened more than once during a session, it's only counted once.

</td></tr><tr><td>

Page views

</td><td>

Shows number of views of the selected page and the number of users who visited it.

</td></tr><tr><td>

Avg. Duration

</td><td>

Shows the average time spent on the page and the percentage of time spent on the page relative to the time spent throughout the app during sessions.

</td></tr><tr><td>

Avg. Load Time

</td><td>

Shows the average time it takes to load the page, based on the number of times the page is viewed.

</td></tr><tr><td colspan="2">

**Performance****Note:** The sampled data represents 5–10% of the total data that is collected in real time.

</td></tr><tr><td>

Performance graph

</td><td>

Displays the daily, weekly, or monthly performance trend of selected trace types in a graphical representation. From the menu arrow, select one of the following trace types: Browser Time, Server Time, Page Load Time, and Network Time. The Performance graph collects data from the installation of Yokohama patch 1.

![Performance graph.](../../../use/par-for-workspace/image/uxa-web-page-performance-graph.png)

</td></tr><tr><td>

Page Load Time

</td><td>

Overall time to deliver the page by subtracting the time the user requests the page from the time the page is fully rendered in the browser.

</td></tr><tr><td>

Server Time

</td><td>

Time the server takes to process the transaction.

</td></tr><tr><td>

Network Time

</td><td>

Time the network takes to process the request. Calculated by subtracting the time of the user's request from the time the page starts loading in the browser, and then subtracting the server processing time.

</td></tr><tr><td>

Client Time

</td><td>

Time the browser takes to deliver the page by subtracting the time the page is fully rendered from the time the page starts loading in the browser.

</td></tr><tr><td colspan="2">

**Navigation**

</td></tr><tr><td>

Previous page

</td><td>

Shows the top pages from which users arrived to the selected page. Also, the percentage of sessions arriving from each page relative to the total number of navigations to it. Rare actions may be omitted.

</td></tr><tr><td>

Next page

</td><td>

Shows the top pages to which users arrived from the selected page. Also, the percentage of sessions navigating to each page relative to the total number of navigations from it.

</td></tr></tbody>
</table>## Filter options

You can filter the page by date range, user type, and country by default. Using the **Add filter** option, you can filter on other fields including Locale and Role.

**Note:** The Add filter options use a logical AND operator. The results must meet both the criteria in the default filters AND the criteria in the additional filters to be included in the visualizations.

## View page analytics

See user actions, performance and navigation analytics for each page.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Usage Insights**.

2.  Select an application and then select **Data Foundation** &gt; **Pages**.

    For mobile applications, select **Data Foundation** &gt; **Screens**.

3.  Scroll the pages list, or use the Search icon \(![Search icon.](../../../use/navigation/image/IconSearch.png)\) to locate and select a page.


