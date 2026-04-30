---
title: Considerations when creating a time series widget
description: To create a time series widget that fulfills your business goal, keep several points in mind.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Time series widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Considerations when creating a time series widget

To create a time series widget that fulfills your business goal, keep several points in mind.

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

When you are creating a time series widget, consider the following points:

-   To show a filtered set of scores in a time series widget, apply a breakdown to the widget. Only the scores that match the specified element of the breakdown will appear.
-   To show aggregated scores, such as a seven-day average or a sum, apply a time series to the widget.
-   To show the scores of secondary indicators over the same time line, add widget indicators to an existing widget. For more information, see [Add widget indicators](../task/add-indicators-to-widget.md).
-   When you are selecting a visualization for a time series, consider whether you want to emphasize the trend in the scores or specific changes in the scores. Also consider whether you want to show one indicator or compare several related indicators.
-   Rounded calculations based on averages may be off by a small amount due to rounding errors.

