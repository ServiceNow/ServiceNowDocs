---
title: Interactive Filters
description: Interactive Filters allow you to filter all reports on a dashboard dynamically, without modifying the original reports.
locale: en-US
release: xanadu
product: Interactive Filters
classification: interactive-filters
topic_type: concept
last_updated: "2025-05-20"
reading_time_minutes: 2
breadcrumb: [Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Interactive Filters

Interactive Filters allow you to filter all reports on a dashboard dynamically, without modifying the original reports.

You can create an interactive filter and add it to a dashboard as a widget. Selecting a value in the Interactive Filter widget filters the data in reports on the dashboard. On dashboards, selected filters are saved for each user and applied automatically the next time that user views the dashboard.

Core UI interactive filter functionality is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed. For updated filtering functionality, see [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

To create an interactive filter, see [Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md) and choose the filter type.

Interactive filters on homepages do not retain default values or retain values across logins or page refreshes. This functionality is available on dashboards. For more information, see [Convert homepages to individual dashboards](../task/hpm-convert-homepages.md).

**Important:**

-   Performance Analytics widgets on the dashboard do not follow interactive filters. Separately filter those widgets on the same [breakdown source](../../performance-analytics/concept/breakdown-sources.md) by using the breakdown dashboard controls. For more information, see [Using breakdowns on dashboards](../../performance-analytics/concept/c_SpecialDashboards.md) and [Make a breakdown act as an interactive filter](../task/make-breakdown-interactive-filter.md).
-   Interactive filters are not supported for reports that are based on a MetricBase source. For more information, see [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

For information about unified filters in Platform Analytics, see [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

-   **[Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md)**  
You can create and configure Interactive Filters for multiple field types.
-   **[Interactive Filters on dashboards](c_PublishersOnHomepages.md)**  
You can make an Interactive Filter available to users by adding the filter to a dashboard.
-   **[Custom interactive filters](c_CustomPublishers.md)**  
As an administrator, you can create scripted interactive filter widgets to provide advanced filtering options on dashboard reports.

**Parent Topic:**[Reporting, dashboards, and Performance Analytics in the Core UI](../../reporting/concept/classic-vis-overview.md)

