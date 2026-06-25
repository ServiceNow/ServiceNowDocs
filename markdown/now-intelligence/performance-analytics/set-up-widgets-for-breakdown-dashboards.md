---
title: Configure widgets for breakdown dashboards
description: Configure each widget that goes on a breakdown dashboard. The configuration determines whether and how the widget follows the elements selected on the dashboard. For some widgets and indicators, you can select whether to show multiple element values separately or as an aggregate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/set-up-widgets-for-breakdown-dashboards.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using breakdowns on dashboards, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Configure widgets for breakdown dashboards

Configure each widget that goes on a breakdown dashboard. The configuration determines whether and how the widget follows the elements selected on the dashboard. For some widgets and indicators, you can select whether to show multiple element values separately or as an aggregate.

## Before you begin

This task assumes that you are starting from an open breakdown dashboard.

Role required: pa\_power\_user, admin

## Procedure

1.  On the breakdown dashboard, click the plus sign \(\[Omitted image "AddWidgetButton.png"\] Alt text: Plus sign button\) to put the dashboard in edit mode.

2.  Point to the widget, then click the pencil icon \(\[Omitted image "EditWidgetButton.png"\] Alt text: Pencil icon\).

    The widget record opens.

3.  Select **Follow element** in the widget record.

    \[Omitted image "follow-element.png"\] Alt text: Section of widget properties form with Follow element selected

    If you do not select **Follow element** for a widget, that widget does not follow any breakdown elements selected on the dashboard. The **Followed breakdown** and **Show multiple elements as** options are not visible.

    If the widget is for a formula indicator, all contributing indicators in the formula must support the selected breakdown source on the dashboard. Otherwise, no scores are displayed in the widget. In this case, a message displays to inform you of the situation.

    **Important:** Do not specify a breakdown and element on the widget record when you want the elements for that breakdown to be selected on a breakdown dashboard. The element on the widget record overrides any elements selected on the breakdown dashboard for that breakdown.

4.  If more than one breakdown uses one of the breakdown sources on the dashboard, specify which breakdown applies to the widget in **Followed breakdown**.

    For example, the breakdowns Opened by, Requested by, Requested for, and Assigned to use the Users.Active breakdown source. If you add Users.Active to a dashboard, select the relevant breakdown in **Followed breakdown** for each of the widgets that you have on that dashboard. This option does not affect any other breakdown sources you may have added to the dashboard.

5.  In the **Show multiple elements as** field, select how to show scores when a dashboard viewer selects multiple breakdown elements.

    Choose from two possibilities:

    -   **Aggregate**, which shows a single, aggregate score of all selected elements.
    -   **Separate**, which shows each selected element separately.
    Not all widget and indicator types support both views. Some types do not support selecting multiple elements at all. If it is not possible to select multiple elements for a widget/indicator combination, the field says **Not available**. For more information, see [Showing multiple elements separately or aggregated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/multi-element-select-indicator-views.md).


**Parent Topic:**[Using breakdowns on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_SpecialDashboards.md)

**Related topics**  


[Add breakdown sources to a dashboard]()

[Showing multiple elements separately or aggregated]()

[Same breakdown on widget and dashboard]()

[Showing breakdown relations on dashboards]()

