---
title: Add widgets to a dashboard in Collaborative Work Management
description: Add predefined or custom widgets to an empty state or existing dashboard on a CWM Board to visualize task and sprint data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/collaborative-work-management/add-a-widget-to-cwm-dashboard.html
release: zurich
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 2
keywords: [add widget, dashboard widget, chart widget, dial widget, CWM]
breadcrumb: [Monitor and track work using dashboards in CWM, Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Add widgets to a dashboard in Collaborative Work Management

Add predefined or custom widgets to an empty state or existing dashboard on a CWM Board to visualize task and sprint data.

## Before you begin

A dashboard is created. For more information, see [Create a dashboard for a CWM Board in Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/creating-dashboards-in-cwm.md).

Role required: sn\_cwm.cwm\_user

## About this task

Space owners and editors can add or create widgets.

The Add widgets panel on an empty state dashboard changes to Manage widgets after at least one widget is added to it. For existing dashboards, the panel appears as Manage widgets and displays the **Included in this dashboard** section listing the widgets already on the dashboard. For information about dashboard panels, see [Monitor and track work using dashboards in CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-board-dashboards.md).

For custom widgets, the columns common to CWM task types and other work item types show only the column name, for example **Assigned to**. Columns specific to a connected work type show the column name followed by the work item type in parentheses, for example **Caller \(Incident\)**. All custom columns are also available for widget configuration.

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a Space, select the Board where your dashboard is.

3.  Select the **Dashboard** tab.

4.  Select the dashboard from the Shared dashboards list.

5.  Select **Add widgets** for a new dashboard or **Manage widgets** for an existing dashboard.

    \[Omitted image "cwm-add-widget-empty-state.png"\] Alt text: The Add widget option in an empty state dashboard.

6.  In the Add widgets or Manage widgets panel, browse the available widgets, organized by chart type.

    **Tip:** Use the search field in the widget panel to find a widget.

    \[Omitted image "cwm-add-widgets=panel.png"\] Alt text: The Add widgets panel.

7.  Add a predefined widget or create a custom one.

<table id="choicetable_at1_rhy_hkc"><thead><tr><th align="left" id="d328194e194">

Goal

</th><th align="left" id="d328194e197">

Action

</th></tr></thead><tbody><tr><td id="d328194e203">

**Add a predefined widget**

</td><td>

Select **Add** next to a predefined widget to add it to the dashboard as-is.\[Omitted image "cwm-widget-add-option.png"\] Alt text: Add option for predefined widgets next to the widget name.

</td></tr><tr><td id="d328194e221">

**Create a custom widget**

</td><td>

1.  Select **Create** next to a custom widget.
2.  Enter a name for the chart.
3.  Select the column to use for the widget.

**Tip:** Use the search field in the column list to find a column quickly.

4.  Select **Add**.

This button is inactive until you enter a name and select a column.

</td></tr></tbody>
</table>    The widget is added to the dashboard.

8.  Select **Done** to close the Add widgets or Manage widgets panel.


## Result

The widget appears in the **Included in this dashboard** section of the Manage widgets panel.

\[Omitted image "cwm-included-in-dashboard-widget.png"\] Alt text: The Included in this dashboard section of the Manage widgets panel.

**Parent Topic:**[Monitor and track work using dashboards in CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-board-dashboards.md)

