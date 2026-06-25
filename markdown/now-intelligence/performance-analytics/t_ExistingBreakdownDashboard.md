---
title: Add breakdown sources to a dashboard
description: To enable dashboard users to filter visualizations on a dashboard by breakdown element, add breakdown sources to the dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/t\_ExistingBreakdownDashboard.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using breakdowns on dashboards, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Add breakdown sources to a dashboard

To enable dashboard users to filter visualizations on a dashboard by breakdown element, add breakdown sources to the dashboard.

## Before you begin

Role required: pa\_admin, pa\_power\_user, or admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Open the relevant dashboard.

3.  From the context menu, select **Dashboard Properties**.

    \[Omitted image "dashboard-context-menu.png"\] Alt text: Dashboard context menu

    The dashboard record opens.

4.  Click **Edit** in the Breakdown Source related list.

    \[Omitted image "dashboard-breakdown-sources.png"\] Alt text: The Edit button on the Breakdown Source related list

    A dialog opens where you can move breakdown sources into and out of the list.

5.  Move the breakdown sources you want to apply to the Breakdown Source List.

6.  Click **Save**.


## Result

The breakdown sources are available on the dashboard. Users can group the dashboard on the selected elements.

## What to do next

-   You can configure the entries in the Breakdown Source related list so that reports on the dashboard can use the breakdown sources as interactive filters. You first create interactive filters that are based on the same tables as the breakdown sources. For more information, see [Make a breakdown act as an interactive filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/core-ui-interactive-filters/make-breakdown-interactive-filter.md).
-   Configure the Performance Analytics widgets on the dashboard so that users can filter them by selecting breakdown elements on the dashboard. For more information, see [Configure widgets for breakdown dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/set-up-widgets-for-breakdown-dashboards.md).


**Parent Topic:**[Using breakdowns on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_SpecialDashboards.md)

**Related topics**  


[Configure widgets for breakdown dashboards]()

[Showing multiple elements separately or aggregated]()

[Same breakdown on widget and dashboard]()

[Showing breakdown relations on dashboards]()

