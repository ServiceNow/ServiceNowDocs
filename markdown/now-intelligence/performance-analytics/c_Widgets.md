---
title: Performance Analytics widgets
description: Widgets enable you to define visualizations for indicator scores. Widgets are shown on dashboards.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Performance Analytics widgets

Widgets enable you to define visualizations for indicator scores. Widgets are shown on dashboards.

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

A Performance Analytics widget ties an indicator to a visualization, such as a trend line, a set of columns, or a pie chart. Within the widget, you can filter or group indicator scores by breakdowns. You can also apply time series functions, such as 7-day sums, to the scores.

To create or edit a Performance Analytics widget, the user must have the pa\_admin or pa\_power\_user role. These roles are also required to add widgets to a dashboard. However, any user can view a widget that has been added to a dashboard.

**Note:** If a user is prevented from viewing a visualization, a warning message prompts the user to contact the administrator.

If the dashboard is so configured, you can select breakdown elements on the dashboard that apply to all the widgets on the dashboard. If you click a score in a widget on a dashboard, you open the Analytics Hub focused on that indicator.

**Note:** Time series aggregations are validated on the Analytics Hub and in KPI Details but not in widgets. Therefore, you might navigate from a working widget to the Analytics Hub and get a warning that the indicator has an invalid aggregation.

## Rounding off

Values between 10,000 and 999,999 are rounded off to the nearest thousand and abbreviated with a K, such as 11K for 11,234. Values between 1 million and 999,999,999 are rounded off to the nearest million and abbreviated with an M. Values of 1 billion and higher are rounded off to the nearest billion and abbreviated with a G.

Rounded calculations based on averages may be off by a small amount due to rounding errors.

## Widget types and creation details

The first step in creating a widget is to select the type of widget to create. Base this decision on the business goals you are trying to achieve with the widget.

|Widget type|Purpose|Typical Visualizations|
|-----------|-------|----------------------|
|[Time Series widget](../reference/time-series-widgets.md)|Shows changes over time in indicator scores.|Line visualization is the most usual. Other visualizations are: spline, step, column, stacked column, area, and relative compare.|
|[Breakdown widget](../reference/breakdown-widgets.md)|Groups indicator scores by the elements of a breakdown.|Scorecard, pie and similar charts, funnel and pyramid, column and similar charts, relative compare, line, Pareto, pivot scorecard, and treemap.|
|[Score widget](../reference/score-widgets.md)|Shows aggregate indicator scores. Can show an indicator score against a target.|Latest score, speedometer, real-time score.|
|[List widget](../reference/list-widgets.md)|Lists the metrics for several indicators.|Scorecard, spider web.|
|[Pivot widget](../task/create-heatmap-pivot-widget.md)|Groups the scores of one indicator by the elements of two breakdowns.|Heatmap|
|[Text analytics](text-analytics-widgets.md)|Visualizes word frequencies and groupings in the text that users enter in forms|Word cloud|
|[Workbench widget](c_MonitorWorkflowWorkbenchWidget.md#)|Shows multiple indicators and their relations, to monitor a workflow or other process.|Workbench|

## Security requirements for viewing widgets

Starting with Quebec, widgets follow indicator and breakdown access control lists \(ACLs\). Outside of ACLs, no roles are required for viewing widgets.

However, if you upgrade an instance from a version earlier than Quebec, by default the rules from before Quebec still apply. Indicator and breakdown ACLs are followed only in these areas:

-   List widgets follow indicator ACLs.
-   When viewing breakdowns, breakdown ACLs apply.

Furthermore, on an upgraded instance, the following widgets may require users to have the pa\_viewer role:

-   List widgets
-   Text widgets
-   The Breakdowns section of Workbench widgets

Upgraded instances cannot automatically follow the rules introduced in Quebec because of the variation in how ACLs are configured.

## Data tables for widget accessibility

If under Preferences you have enabled **Accessibility** &gt; **Enable data table for charts and graphs**, tables replace the graphical charts for all Performance Analytics widgets on your instance. Workspace widgets are an exception, as they show both charts and tables. For more information about accessibility and widgets, including how to replace colors with patterns, see [Accessibility options on dashboards](../../reporting/concept/analytics-accessibility-options.md).

![Workbench widget with the Data tables accessibility preference activated, showing both a chart and a table.](../image/widget-accessibility-table.png)

