---
title: Using breakdowns on dashboards
description: You can add breakdown sources to a dashboard. Dashboard users then can select a breakdown source and one or more breakdown elements to filter scores in the visualizations on the dashboard.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Using breakdowns on dashboards

You can add breakdown sources to a dashboard. Dashboard users then can select a breakdown source and one or more breakdown elements to filter scores in the visualizations on the dashboard.

The selected elements filter those Performance Analytics widgets on the dashboard that follow these conditions:

-   An indicator on the widget uses a breakdown that is based on the selected breakdown source. For formula indicators, all the contributing indicators in the formula must use a breakdown based on this source.
-   The widget follows elements on breakdown dashboards.

The selected elements filter reports on the dashboard under the following conditions:

-   You have configured the dashboard to use the breakdown source as an interactive filter.
-   The report follows interactive filters on the dashboard.

If the dashboard user selects multiple elements, widgets can show scores separately for those elements, or show a single aggregate, depending on the widget type and configuration. For more information, see [Showing multiple elements separately or aggregated](../../dashboards/concept/multi-element-select-indicator-views.md).

**Note:** If you show a breakdown relation on a widget, that widget cannot show multiple elements. For more information, see [Showing breakdown relations on dashboards](c_ShowBkdwnRltnsWdgts.md).

The following illustration shows a breakdown widget with the scores given separately for each selected element of the Category breakdown. The dashboard user has selected three elements of the Incident.Category breakdown source. If this user has access to the Analytics Hub, they can click any score to view the score trend in the Analytics Hub.

![Dashboard with multiple breakdown elements applied from the Category breakdown](../image/breakdown-db-with-mes3.png "Time series widget on breakdown dashboard")

**Note:** If you view a breakdown dashboard with a breakdown applied but no elements, the widgets show the base indicator scores. The breakdown does not filter the scores. These scores are usually higher than the scores when you select a breakdown and all elements. Often not all elements are available due to element security or an element filter. You also usually cannot select the Unassigned score, which contributes to the indicator scores.

-   **[Add breakdown sources to a dashboard](../../dashboards/task/t_ExistingBreakdownDashboard.md)**  
To enable dashboard users to filter visualizations on a dashboard by breakdown element, add breakdown sources to the dashboard.
-   **[Configure widgets for breakdown dashboards](../task/set-up-widgets-for-breakdown-dashboards.md)**  
Configure each widget that goes on a breakdown dashboard. The configuration determines whether and how the widget follows the elements selected on the dashboard. For some widgets and indicators, you can select whether to show multiple element values separately or as an aggregate.
-   **[Showing multiple elements separately or aggregated](../../dashboards/concept/multi-element-select-indicator-views.md)**  
When you select multiple elements on a dashboard, widgets that follow these elements can show their values either separately or as an aggregate.
-   **[Same breakdown on widget and dashboard](same-breakdown-widget-dashboard.md)**  
If a widget uses the same breakdown as the dashboard, the dashboard breakdown does not apply.
-   **[Showing breakdown relations on dashboards](c_ShowBkdwnRltnsWdgts.md)**  
A breakdown widget can display 1st level breakdown elements that are related to the element selected for the dashboard. The widget must be on a breakdown dashboard, and that dashboard must include the breakdown sources of the related breakdowns.

**Parent Topic:**[Indicator breakdowns](c_CreatingBreakdowns.md)

**Related topics**  


[Performance Analytics widgets](c_Widgets.md)

[Indicator breakdowns](c_CreatingBreakdowns.md)

[Define a breakdown source](../task/t_DefiningABreakdownSource.md)

[Analytics Hub for a specific indicator](view-scorecard.md)

[Make a breakdown act as an interactive filter](../../dashboards/task/make-breakdown-interactive-filter.md)

