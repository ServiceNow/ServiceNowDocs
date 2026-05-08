---
title: Enable real-time updating for single score report widgets
description: Real-time updates ensure that users viewing a responsive dashboard always see the most up-to-date information.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Enable real-time updating for single score report widgets

Real-time updates ensure that users viewing a responsive dashboard always see the most up-to-date information.

## Before you begin

Role required: You must have edit rights to the dashboard where the widget has been added.

Four types of aggregation are available for single-score reports: Count, Average, Sum, and Count Distinct. Real-time updating is available only for single score widgets that use the **Count** aggregation.

**Note:** Real-time updating doesn’t work for single score reports on responsive dashboards under the following circumstances:

-   When the report source is a [database view](../../performance-analytics/concept/performance-analytics-glossary.md#), the user must click the Refresh icon ![Refresh icon](../image/icon-refresh.png) on the widget to update the score. For more information, see Database views.
-   Domain visibility is not supported in real-time reporting. Only the assigned domain of the user and its domain hierarchy and, the global domain are supported.
-   When the visualization has dot-walked conditions, the single score report doesn’t update when there’s a related change on the extended table. The record watcher only sends updates on the base table of the report. For more information, see [KB article KB0868215](https://support.servicenow.com/kb_view.do?sysparm_article=KB0868215).
-   When a business rule that uses the `current.update()` method fires on insert/update, the single score report increments by two instead of one. For more information, see [KB article KB0693812](https://support.servicenow.com/kb_view.do?sysparm_article=KB0693812).
-   Conditions that are added or modified by query business rules are not respected in real-time reporting.

    Because query business rules change query conditions on the fly for the specific user, the record watcher framework used for real-time updates doesn't trigger the query business rules.

-   When a widget uses the filter `Assignment group - is (dynamic) - One of My Groups`, the widget doesn’t update in real time.
-   Single score report real time update is not supported on rotation tables, Workflow Data Fabric tables, and remote tables.

## About this task

You can enable real-time updating for single score widgets on dashboards.

## Procedure

1.  Navigate to the dashboard where the single score widget has been added.

2.  Click the Add widgets icon\(![Add widgets icon - a plus inside of a circle](../image/icon-add-user-db.png)\) to put the dashboard in edit mode.

3.  Point to the widget, then click the gear icon \(![Gear icon](../../performance-analytics/image/Cogwheel.png)\).

4.  Select **Show real-time updates** then click **Done**.

5.  Click the plus sign \(![Plus sign button](../image/AddWidgetButton.png)\) to exit edit mode for the dashboard.

    The real-time icon \(![Real time icon](../image/real-time-update-icon.png)\) is added to the widget. This icon is permanently visible, even when the score isn’t changing.


## Result

When the value for a single score visualization changes, the change is reflected on the dashboard.

