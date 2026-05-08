---
title: Configure a Date filter in the inline editor
description: Let users select predefined periods or specify custom start and end dates for the data on a dashboard tab.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# Configure a Date filter in the inline editor

Let users select predefined periods or specify custom start and end dates for the data on a dashboard tab.

## Before you begin

**Important:** This procedure assumes you’ve created a filter in the Filter designer or added a filter to your dashboard with the Date filter type. For instructions, see [Create or add a filter on an inline dashboard](select-workspace-filter-type.md) or [Create a filter in the Filter Designer](add-filter-library.md).

Role required: In the dashboard inline editor: dashboard\_admin, or you must be the dashboard owner or have had editing rights shared with you.

In the Filter Designer \(**Library** &gt; **Filters** &gt; **New**\): analytics\_filter\_admin, admin

## About this task

Date filters apply to Score, Time series, Bar, and Pie/Donut visualizations. For indicator data, the **Apply date range** option must be turned on in the visualization's configuration panel \(except for time series, where it's implicitly always on\). The filter applies to all such visualizations in the same dashboard or dashboard tab as the filter.

For time series data visualizations showing table or indicator data, the data aggregation on those visualizations adjusts automatically to follow the date range selected in the filter.

## Procedure

1.  Create a filter and select the Date filter type, as described in [Create or add a filter on an inline dashboard](select-workspace-filter-type.md) or [Create a filter in the Filter Designer](add-filter-library.md).

2.  Specify the data to filter.

    The filter is applied automatically to all Performance Analytics indicators and MetricBase KPIs on the tab or in the dashboard.

    ![Data to filter section with KPIs added automatically.](../image/filter-all-kpis.png)

    You can add any number of date fields on tables or Usage Insights date properties to apply the filter to. If you add a table field, you can also choose to apply the filter to the hierarchy of related tables: Parents, children, siblings, and any database views that contain the table.

3.  In **Date filter view**, select the options that the runtime user has for choosing date ranges:

    -   Choice of calendar dates or relative ranges, such as seven days or Year To Date \(YTD\)
    -   Calendar only
    -   Relative ranges only
    ![Runtime view of date filter with both relative ranges and calendar.](../image/paw-filter-calendar-rel-ranges.png)

4.  If you’re letting the users select from relative ranges, you can select which relative ranges they can choose from in **Select predefined ranges**.

    If you have Fiscal Calendars installed and configured, you can select from fiscal calendar ranges. For more information, see Defining fiscal calendars.

    ![Select Predefined Ranges picker showing fiscal calendar options.](../image/filters-fiscal-calendar.png)

5.  To let users filter on the time in hours and minutes instead of only the date, enable **Allow time selection**.

6.  In **Default values**, specify a relative range to filter on automatically when the dashboard is opened.

7.  To let users clear the values they selected for the filter, enable **Allow filter clearance**.

8.  Select **Save**.


## Result

The filter is ready to use when you exit editing mode.

## What to do next

If you have the required roles, add the filter to the filter library. You can also reconfigure, delete, or duplicate the filter. For more information, see [Edit a Platform Analytics filter on a dashboard](edit-filters-configurable-workspaces.md).

**Related topics**  


[Edit a Platform Analytics filter on a dashboard](edit-filters-configurable-workspaces.md)

[Configure a data visualization to follow filters or not](configure-dv-follow-filters-or-not.md)

