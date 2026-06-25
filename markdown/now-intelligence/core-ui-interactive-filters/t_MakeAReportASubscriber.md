---
title: Make a report follow interactive filters
description: When you add interactive filters to a Core dashboard, you can configure the reports on the dashboard to accept input from interactive filters. For example, you add a filter on the Incident table's Active field. Reports on the Incident table can reflect the user's choice from that filter.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/core-ui-interactive-filters/t\_MakeAReportASubscriber.html
release: australia
product: Core UI Interactive Filters
classification: core-ui-interactive-filters
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Interactive Filters on dashboards, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Make a report follow interactive filters

When you add interactive filters to a Core dashboard, you can configure the reports on the dashboard to accept input from interactive filters. For example, you add a filter on the Incident table's Active field. Reports on the Incident table can reflect the user's choice from that filter.

## Before you begin

Role required: report\_admin

## About this task

**Note:** This task refers to interactive filters in the Core UI. For information about filters in Platform Analytics experience, see [Filters in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/interactive-filters-workspace.md).

Interactive Filters allow you to filter all reports on a dashboard dynamically, without modifying the original reports. To be effective, interactive filters must be based on the same tables as the reports they filter. Reports based on the user table, for example, do not follow Interactive Filters that are based on the incident table.

## Procedure

1.  Navigate to a dashboard.

2.  Put the dashboard in edit mode.

3.  In the report widget, select the Edit widget icon \(\[Omitted image "Pa\_dashboard\_cog.png"\] Alt text: Edit widget icon\).

4.  Select **Follow interactive filter**.

    This option is available for all report widgets. If you don’t see the **Follow interactive filter** option, the widget is a list, PA, or other non-report widget.

5.  To show a filter icon \(\[Omitted image "InteractiveFilterFilteringIcon.png"\] Alt text: Filter icon\) on the top-left corner of the report when it’s following an interactive filter, select **Show when following**.

6.  Select **Done**.

7.  Refresh the current browser page to apply the change.


## What to do next

Add one or more interactive filters to the dashboard.

**Parent Topic:**[Interactive Filters on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/core-ui-interactive-filters/c_PublishersOnHomepages.md)

**Related topics**  


[Add an interactive filter widget to a responsive dashboard]()

[Make a breakdown act as an interactive filter]()

[Make a report act as an interactive filter]()

[Reset all interactive filters on a dashboard tab]()

[Edit a responsive dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_EditADashboard.md)

