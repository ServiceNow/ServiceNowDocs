---
title: Filter dashboards on breakdown elements
description: Some dashboards let you apply one or more Performance Analytics breakdown elements to filter the entire dashboard. For example, you can show only high and critical priority items or only the teams that report to a certain manager.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Filter dashboards on breakdown elements

Some dashboards let you apply one or more Performance Analytics breakdown elements to filter the entire dashboard. For example, you can show only high and critical priority items or only the teams that report to a certain manager.

## Before you begin

You must have a dashboard already created with the Performance Analytics that you want to filter by breakdown element. Dashboards that have been configured in this way are called breakdown dashboards.

Role required: None

## About this task

To filter a dashboard on breakdown elements, such as priorities or categories, select the breakdown source and then select elements within that breakdown source. Reports and appropriately configured Performance Analytics widgets reflect the filter when it is applied. If you select multiple elements, Performance Analytics shows the values associated with those elements as an aggregation or as separated elements, depending on how each Performance Analytics widget is configured. For more information about configuring breakdown dashboards and their widgets, see [Using breakdowns on dashboards](../../performance-analytics/concept/c_SpecialDashboards.md).

For performance reasons, there is no option to select all breakdown elements.

**Note:** If you view a breakdown dashboard with a breakdown applied but no elements, the widgets show the base indicator scores. The breakdown does not filter the scores. These scores are usually higher than the scores when you select a breakdown and all elements. Often not all elements are available due to element security or an element filter. You also usually cannot select the Unassigned score, which contributes to the indicator scores.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select the dashboard that you want to filter by breakdown elements.

3.  Select a breakdown source from the list in the upper left.

    ![Dashboard widget with breakdown source list open and the source Incident.Category highlighted.](../image/select-breakdown-source-mes.png)

4.  In the Select Elements list, select the element or elements you want to filter on and click **Apply**.![Database, Hardware, Network, and Software breakdown elements selected on a breakdown dashboard, only the Selected elements are shown, and the sort order is A-Z](../../performance-analytics/image/breakdown-db-with-mes-2-ny-db.png)

    The widgets on the dashboard that can be filtered are filtered on the selected elements. Next to their titles, filtered widgets show a filter icon ![Green filter icon shown in widgets that are filtered](../image/green-filter-icon.png).

    **Note:** If element security settings prevent you from seeing one or more selected elements, a warning appears.

5.  Click **Selected** to show only the selected breakdown elements.

    Click **All** to show all of the breakdown elements in the list.

6.  Click **Sort** to sort the list of elements in alphabetical order.

    The direction of the triangle indicates a-z or z-a.

7.  Select a data point to show the indicator and breakdown elements in the Analytics Hub.

    Access to the Analytics Hub requires the pa\_viewer role.

    Targets, thresholds, and comments are not available when you navigate to the Analytics Hub from a widget with multiple breakdown elements selected in an aggregate view. The breakdown selector and search functionality are also unavailable. For more information about aggregate and separate views of multiple elements in a widget, see [Configure widgets for breakdown dashboards](../../performance-analytics/task/set-up-widgets-for-breakdown-dashboards.md).

8.  Select **Clear all** to remove the selected elements and show the breakdown widget with all elements.


