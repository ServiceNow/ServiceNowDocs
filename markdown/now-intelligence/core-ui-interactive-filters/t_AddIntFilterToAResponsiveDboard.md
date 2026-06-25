---
title: Add an interactive filter widget to a responsive dashboard
description: Add an interactive filter to a dashboard to filter reports on that dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/core-ui-interactive-filters/t\_AddIntFilterToAResponsiveDboard.html
release: australia
product: Core UI Interactive Filters
classification: core-ui-interactive-filters
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Interactive Filters on dashboards, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Add an interactive filter widget to a responsive dashboard

Add an interactive filter to a dashboard to filter reports on that dashboard.

## Before you begin

Role required: The dashboard\_admin role is required to create or edit Core UI Responsive Dashboards, which may still be necessary in Service Portal, for example. You must have edit access to the dashboard you want to add the widget to.

## About this task

To be effective, interactive filters must be based on the same tables as the reports they filter. Reports based on the user table, for example, do not follow Interactive Filters that are based on the incident table. For more information, see [Make a report follow interactive filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/core-ui-interactive-filters/t_MakeAReportASubscriber.md).

For more information on which interactive filters are available, see [Creating Interactive Filters of different types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/core-ui-interactive-filters/r_AvailableHomepagePublisherTypes.md). From this topic you can learn more about creating and configuring the different filters.

In this animation, the two visualizations and the interactive filter are all based on the incident table. Both visualizations are configured to follow filters. When you select one of the filter options, in this case, Active is true, Active is False, or All, both visualizations refresh to follow the choice.

\[Omitted image "if-example.gif"\] Alt text: Dashboard with a filter and two visualizations that follow it - a single score and a bar chart. The animation flows through the filter choices: All, true, and false.

## Procedure

1.  Navigate to a Core UI dashboard.

2.  Click the add content icon \(\[Omitted image "AddWidgetButton.png"\] Alt text: Add content icon \).

3.  Select **Interactive filters**.

4.  Select the type of filter to add, such as **Choice list** or **Reference**.

    You can also add a new filter. For more information, see [Creating Interactive Filters of different types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/core-ui-interactive-filters/r_AvailableHomepagePublisherTypes.md).

5.  Select the filter you want to add.

6.  Click **Add** or drag the filter onto the dashboard.

    \[Omitted image "add-if-resp-db.gif"\] Alt text: Animated gif showing the steps to add an interactive filter to a dashboard


**Parent Topic:**[Interactive Filters on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/core-ui-interactive-filters/c_PublishersOnHomepages.md)

**Related topics**  


[Make a breakdown act as an interactive filter]()

[Make a report follow interactive filters]()

[Make a report act as an interactive filter]()

[Reset all interactive filters on a dashboard tab]()

