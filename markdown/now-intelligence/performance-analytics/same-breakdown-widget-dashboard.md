---
title: Same breakdown on widget and dashboard
description: If a widget uses the same breakdown as the dashboard, the dashboard breakdown does not apply.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using breakdowns on dashboards, Performance Analytics breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Same breakdown on widget and dashboard

If a widget uses the same breakdown as the dashboard, the dashboard breakdown does not apply.

When you design a widget, you can specify up to two levels of breakdown to apply to that widget. Then you can add that widget to any dashboard, including a breakdown dashboard. If one of the breakdowns for the dashboard is the same as one of the breakdowns of the widget, that dashboard breakdown does not affect the widget. The behavior for that breakdown is the same as though **Follow element** was disabled for this widget.

If you add a breakdown type widget with interactive breakdown selection to a dashboard, this limitation does not fully apply. When the user selects the same breakdown on the widget and on the dashboard, the dashboard breakdown is ignored. However, when the user selects any other combination of widget and dashboard breakdowns, both breakdowns apply.

## Breakdown widget on a breakdown dashboard

In the following animation, you have a breakdown widget on a breakdown dashboard. The widget has **Follow element** selected in its configuration. Both the dashboard and the widget are using elements of the Category breakdown. When you select elements on the dashboard, it has no effect on the widget. Then you select the Urgency breakdown on the widget. Now selecting elements on the dashboard does affect the widget. If you had changed the breakdown source on the dashboard instead of the breakdown on the widget, selecting elements on the dashboard also would have affected the widget.

![A breakdown widget on a breakdown dashboard, first with the same breakdown selected, then with a different breakdown selected](../image/interactive-bkdown-widget-on-bkdown-dashboard.gif "Widget with interactive breakdown selection on a breakdown dashboard")

**Parent Topic:**[Using breakdowns on dashboards](c_SpecialDashboards.md)

**Related topics**  


[Add breakdown sources to a dashboard](../../dashboards/task/t_ExistingBreakdownDashboard.md)

[Configure widgets for breakdown dashboards](../task/set-up-widgets-for-breakdown-dashboards.md)

[Showing multiple elements separately or aggregated](../../dashboards/concept/multi-element-select-indicator-views.md)

[Showing breakdown relations on dashboards](c_ShowBkdwnRltnsWdgts.md)

