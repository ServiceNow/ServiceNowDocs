---
title: Make a report act as an interactive filter
description: You can configure an existing report widget to filter other report widgets on the same dashboard.
locale: en-US
release: yokohama
product: Interactive Filters
classification: interactive-filters
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Interactive Filters on dashboards, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Make a report act as an interactive filter

You can configure an existing report widget to filter other report widgets on the same dashboard.

## Before you begin

Role required: itil, report\_user.

Only reports with a **Type** value of pie, donut, semi donut, funnel, or pyramid can act as interactive filters.

**Note:**

-   When a report is acting as an interactive filter, it is not possible to drill down into the report's segments.
-   This documentation refers to Core UI reports and interactive dashboards. For information about making Platform Analytics data visualizations act as filters on dashboards, see [Make a data visualization act as a filter](../../par-for-workspace/task/make-dv-act-as-filter.md).

## Procedure

1.  Navigate to a dashboard.

2.  Put the dashboard into Edit mode.

    -   On a non-responsive dashboard, select **Edit**.
    -   On a responsive dashboard, click the sharing icon \(![](../image/SharingIcon.png)\).
3.  Point to the top of the report widget, and click the Edit widget icon \(![](../image/Pa_dashboard_cog.png)\).

4.  Select **Act as interactive filter**.

    This field is only available on reports that can act as filters. Only reports with a **Type** value of pie, donut, semi donut, funnel, or pyramid can act as filters.

    **Note:** When responsive canvas functionality is inactive, there’s no delay in filtering when a user clicks segments of a report that acts an interactive filter in quick succession.

5.  Select **Done**.

6.  Refresh the current browser page to apply the change.


## What to do next

Select a subset of data in the report, such as a slice of pie in a pie chart, to filter all subscriber reports for the same table. All reports on the dashboard that are based on the same table show information about that subset of data only.

**Parent Topic:**[Interactive Filters on dashboards](../concept/c_PublishersOnHomepages.md)

**Related topics**  


[Add an interactive filter widget to a responsive dashboard](t_AddIntFilterToAResponsiveDboard.md)

[Make a breakdown act as an interactive filter](make-breakdown-interactive-filter.md)

[Make a report follow interactive filters](t_MakeAReportASubscriber.md)

[Reset all interactive filters on a dashboard tab](reset-all-filters.md)

