---
title: Showing multiple elements separately or aggregated
description: When you select multiple elements on a dashboard, widgets that follow these elements can show their values either separately or as an aggregate.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using breakdowns on dashboards, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Showing multiple elements separately or aggregated

When you select multiple elements on a dashboard, widgets that follow these elements can show their values either separately or as an aggregate.

On a widget form, use the **Show multiple elements as** field to set whether multiple elements are shown separately or as an aggregate. Widgets with the view type **Separate** show a different value for each [breakdown element](../../performance-analytics/concept/performance-analytics-glossary.md#) selected. Widgets with the view type **Aggregate** show a single value that represents the aggregated value of all selected breakdown elements.

The widget type logically determines whether an aggregated view, a separate view, or both are available. Also, [formula indicators](../../performance-analytics/concept/performance-analytics-glossary.md#) support the aggregated view only when the aggregated view is explicitly enabled on the indicator record. For example, a Score widget can only show an aggregated view. Without aggregated views being enabled, a Score widget for a formula indicator cannot be filtered on multiple elements. In this case, the **Show multiple element as** field displays **Not available** and is grayed out. For more information, see the section [Indicators that support an aggregate of multiple elements](multi-element-select-indicator-views.md#section_evw_cjx_4hb).

## Widget support of aggregate and separate views

-   Time series widgets support aggregate and separate views.
-   List widgets support aggregate and separate views.
-   Score widgets only support the aggregate view.
-   Breakdown widgets only support the aggregate view.

**Note:** You cannot select multiple elements on workbench or text Performance Analytics widgets. If you try, all selected elements are ignored. This limitation does not apply to Platform Analytics data visualizations.

## Indicators that support an aggregate of multiple elements

The following indicators support the aggregated view:

-   Automated indicators that aggregate data as a Count, Sum, Minimum, or Maximum value

    **Note:** The word "aggregate" is used for two different things here: the aggregate view of multiple indicator scores, and the data aggregation that is set on an indicator.

-   Manual indicators
-   External indicators that do not use `SQL AVG()` or `SQL COUNT(DISTINCT...)` in their SQL statement
-   Formula indicators that have aggregate element views enabled on their indicator records. For more information, see the entry on the **Allow aggregation of multiple breakdown element scores** field on the Other tab in [Create a formula indicator](../../performance-analytics/task/t_CreateAFormulaIndicator.md).

**Important:**

-   Indicators that aggregate data as an Average or a Count Distinct do not support the Aggregate view.
-   The **Show multiple elements as** value applies to both the main widget and any indicator widgets. If **Aggregate** is selected but one of the indicator widgets does not support the **Aggregate** view, that indicator does not follow the elements on the breakdown dashboard. Instead, the indicator follows any first-level breakdown and element that are set in the widget configuration. The other indicators follow the elements on the breakdown dashboard and show an aggregate of their values.

## Results when showing aggregate view

The aggregate view of multiple elements shows a different result depending on the indicator's data aggregation:

|Automated indicator data aggregation|External indicator SQL statement|In a widget, what an aggregate view of multiple elements shows|
|------------------------------------|--------------------------------|--------------------------------------------------------------|
|COUNT|`SQL COUNT()`|A sum of the scores of the selected elements|
|SUM|`SQL SUM()`|A sum of the scores of the selected elements, which themselves are sums|
|MAX|`SQL MAX()`|Whichever element had the highest value at each time point|
|MIN|`SQL MIN()`|Whichever element had the lowest value at each time point|

With the aggregate view selected, not all features are available on all widgets or when the user navigates from the widget to the Analytics Hub:

-   Targets, thresholds, and comments are not available when you navigate to the Analytics Hub from a widget with multiple breakdown elements selected in an aggregate view. The breakdown selector and search functionality are also unavailable.
-   Targets and thresholds are not available in time series widgets.
-   Targets and bullet charts are not available in list widgets.

## Widget indicators and breakdown dashboards

When a user selects breakdown elements on a breakdown dashboard, the breakdown and element names are appended to the widget indicator names. Widget indicator labels also have the breakdown and element names appended. The breakdown and element names are not appended to the widget indicator names and labels in the following circumstances:

-   The widget shows an aggregate view of multiple elements, and the widget indicator does not support this view.
-   The widget does not follow elements.
-   The widget indicators do not support the selected breakdown elements.

![Caption for a time series widget showing indicator names and display labels appended with the breakdown and element names.](../../performance-analytics/image/widget-indicator-labels-separate.png "Names and labels for widget indicators with multiple elements selected, separate view")

![Caption for a time series widget showing indicator names and display labels appended with the breakdown and element name except for where the indicator does not support the aggregate view.](../../performance-analytics/image/widget-indicator-labels-aggregate.png "Names and labels for widget indicators with multiple elements selected, aggregate view")

## Open incidents with aggregate and separate values for multiple elements

Consider a breakdown dashboard with the Incident.Category breakdown source and the three elements Inquiry/Help, Network, and Software selected.![Breakdown dashboard with Incident.Category elements Inquiry/Help, Software, and Network selected.](../../performance-analytics/image/breakdown-dashboard-3-elements.png)

The dashboard contains a time series widget called Open Incidents. This widget shows the Number of Open Incidents indicator, which has the Count aggregate. The widget follows the elements that are selected on the dashboard. Therefore, the widget can show multiple elements selected on the dashboard either separately or as an aggregate value. The **Show multiple elements as** field is set to **Separate**. ![Widget configuration set to show multiple elements separately](../../performance-analytics/image/show-multi-elements-separate.png)

On the dashboard, a separate column is shown for each of the three selected elements for each day. ![Widget showing separate scores for each selected breakdown element](../../performance-analytics/image/separate-multiple-elements.png)

With the **Show multiple elements as** field set to **Aggregate,** a single, aggregate score is shown for the three selected elements. ![Column visualization with a single aggregate score shown for all selected elements](../../performance-analytics/image/aggregate-multiple-elements.png)

**Parent Topic:**[Using breakdowns on dashboards](../../performance-analytics/concept/c_SpecialDashboards.md)

**Related topics**  


[Add breakdown sources to a dashboard](../task/t_ExistingBreakdownDashboard.md)

[Configure widgets for breakdown dashboards](../../performance-analytics/task/set-up-widgets-for-breakdown-dashboards.md)

[Same breakdown on widget and dashboard](../../performance-analytics/concept/same-breakdown-widget-dashboard.md)

[Showing breakdown relations on dashboards](../../performance-analytics/concept/c_ShowBkdwnRltnsWdgts.md)

