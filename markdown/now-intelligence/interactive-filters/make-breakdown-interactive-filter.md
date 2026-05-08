---
title: Make a breakdown act as an interactive filter
description: You can configure a Performance Analytics breakdown on a dashboard to act as an interactive filter for reports on the dashboard. The dashboard must be configured as a breakdown dashboard.
locale: en-US
release: australia
product: Interactive Filters
classification: interactive-filters
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Interactive Filters on dashboards, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Make a breakdown act as an interactive filter

You can configure a Performance Analytics breakdown on a dashboard to act as an interactive filter for reports on the dashboard. The dashboard must be configured as a breakdown dashboard.

## Before you begin

The dashboard should be configured with both reports and Performance Analytics widgets. The dashboard must be configured with at least one breakdown source for the Performance Analytics widgets to follow, as described in [Add breakdown sources to a dashboard](t_ExistingBreakdownDashboard.md). Finally, the dashboard must have an interactive filter that is based on the same table as one of the breakdown sources.

Role required: pa\_power\_user, pa\_admin, or admin

## About this task

When you select a [breakdown](../../performance-analytics/concept/performance-analytics-glossary.md#) and breakdown element on a dashboard, that element can be used to filter reports on the dashboard based on the filtering rules defined in an interactive filter.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select the Core UI dashboard with the breakdown you want to make act as an interactive filter.

3.  Click the context menu icon ![Context menu icon](../../../common/image/Form_MenuIcon.png) and select **Dashboard Properties**.

4.  In the **Breakdown sources** related list, locate the breakdown sources that you want to use as interactive filters.

5.  In the **Act as filter** field for each breakdown source, select the interactive filter you want to use that breakdown source for.

    **Note:** If the **Breakdown sources** list does not have an **Act as filter** column, personalize the list to add one. For more information, see Personal lists.

    The breakdown source **Facts table** must match the table that the interactive filter is based on.

    For example, for the breakdown source HR.Groups.Active, use a reference field interactive filter for the Groups \[sys\_user\_group\] table. Breakdown elements from the HR.Groups.Active breakdown source are not valid selections for interactive filters on other tables, such as interactive filters based on a choice or date field.

    **Note:** You cannot use a breakdown source that is based on a bucket group as an interactive filter.

6.  Click **Update**.

7.  On the dashboard's record, click **View Dashboard**.

8.  Click the + icon to put the dashboard in edit mode.

9.  For each report that you want to follow the interactive filters, follow these steps:

    1.  Click the cog icon ![Cogwheel icon](../../performance-analytics/image/Cogwheel.png) to open the Edit Widget window.

    2.  Select **Follow interactive filter**.

    3.  Select **Show when following filter** to show a filter icon next to the widget title when the widget is following an interactive filter.

10. Click **Done**.


## Result

The selected breakdown acts as an interactive filter on the dashboard's reports.

**Note:** Performance Analytics widgets on the dashboard do not follow interactive filters. Separately filter those widgets on the same breakdown source by using the breakdown dashboard controls. For more information, see [Using breakdowns on dashboards](../../performance-analytics/concept/c_SpecialDashboards.md).

**Parent Topic:**[Interactive Filters on dashboards](../concept/c_PublishersOnHomepages.md)

**Related topics**  


[Add an interactive filter widget to a responsive dashboard](t_AddIntFilterToAResponsiveDboard.md)

[Make a report follow interactive filters](t_MakeAReportASubscriber.md)

[Make a report act as an interactive filter](t_MakeAReportAPublisher.md)

[Reset all interactive filters on a dashboard tab](reset-all-filters.md)

