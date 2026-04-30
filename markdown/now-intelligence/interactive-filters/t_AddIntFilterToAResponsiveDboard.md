---
title: Add an interactive filter widget to a responsive dashboard
description: Add an interactive filter to a dashboard to filter reports on that dashboard.
locale: en-US
release: yokohama
product: Interactive Filters
classification: interactive-filters
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Interactive Filters on dashboards, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Add an interactive filter widget to a responsive dashboard

Add an interactive filter to a dashboard to filter reports on that dashboard.

## Before you begin

Role required: pa\_power\_user. You must have edit access to the dashboard you want to add the widget to.

## About this task

To be effective, interactive filters must be based on the same tables as the reports they filter. Reports based on the user table, for example, do not follow Interactive Filters that are based on the incident table. For more information, see [Make a report follow interactive filters](t_MakeAReportASubscriber.md).

For more information on which interactive filters are available, see [Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md). From this topic you can learn more about creating and configuring the different filters.

In this animation, the two visualizations and the interactive filter are all based on the incident table. Both visualizations are configured to follow filters. When you select one of the filter options, in this case, Active is true, Active is False, or All, both visualizations refresh to follow the choice.

![Dashboard with a filter and two visualizations that follow it - a single score and a bar chart. The animation flows through the filter choices: All, true, and false.](../image/if-example.gif)

## Procedure

1.  Navigate to a dashboard.

2.  Click the add content icon \(![Add content icon](../image/AddWidgetButton.png) \).

3.  Select **Interactive filters**.

4.  Select the type of filter to add, such as **Choice list** or **Reference**.

    You can also add a new filter. For more information, see [Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md).

5.  Select the filter you want to add.

6.  Click **Add** or drag the filter onto the dashboard.

    ![Animated gif showing the steps to add an interactive filter to a dashboard](../image/add-if-resp-db.gif)


**Parent Topic:**[Interactive Filters on dashboards](../concept/c_PublishersOnHomepages.md)

**Related topics**  


[Make a breakdown act as an interactive filter](make-breakdown-interactive-filter.md)

[Make a report follow interactive filters](t_MakeAReportASubscriber.md)

[Make a report act as an interactive filter](t_MakeAReportAPublisher.md)

[Reset all interactive filters on a dashboard tab](reset-all-filters.md)

