---
title: Create a date interactive filter
description: A date interactive filter allows users to filter report widgets based on the value in a date field.
locale: en-US
release: zurich
product: Interactive Filters
classification: interactive-filters
topic_type: task
last_updated: "2026-01-08"
reading_time_minutes: 3
breadcrumb: [Creating Interactive Filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a date interactive filter

A date interactive filter allows users to filter report widgets based on the value in a date field.

## Before you begin

Role required: hp\_publisher\_admin and report\_admin. The hp\_publisher\_admin role exists only for managing interactive filters in Core UI. By default, it contains the role analytics\_filter\_admin for managing Core UI filters that are migrated to Platform Analytics experience.

When a user selects `All`, they do not see a report with all filter options applied, they see the unfiltered report. This example of date filter shows a number of date ranges you can filter on.

![Reference list filter example with the Last 90 days option selected](../image/if-ex-date.png)

**Note:** If the interactive filter has a default value or specifies the last selected value, non-responsive dashboards do not apply this value automatically. This feature is only available on [Responsive dashboards](../concept/c_ResponsiveDashboards.md).

## Procedure

1.  Check the existing interactive filters on the same table.

    1.  Navigate to **sys\_ui\_hp\_publisher.list** and select an interactive filter based on the same table you want to filter.

    2.  Under Related Links, select **Other filters on Table**.

    3.  Review the other filters that are available on the same table to see if the filter you want already exists.

2.  Navigate to **sys\_ui\_hp\_publisher.list**.

3.  Select **New**.

4.  In the **Filter based on** list, select **Date**.

    ![Filter based on list with Date selected](../../reporting/image/if-filter-based-on-date.png)

5.  Set the following fields:

    |Name|Description|
    |----|-----------|
    |Name|Enter a name for the filter. This name appears on the dashboard widget for the filter.|
    |Look up name|Enter a lookup name for the filter. This name appears in the **Add content** menu for users adding a filter to a dashboard. Use this name to help organize your filters. If you do not specify a lookup name, the **Name** value is used instead.|
    |Description|Enter a description of the filter.|
    |UI control type|Select how the available filtering options for this filter appear on the dashboard widget. See [Available interactive filter UI control types](../reference/r_HomepagePublisherUIControlTypes.md).|

6.  Select **Apply to all tables in hierarchy** to apply the filter to parent, child, and sibling tables of an extended table.

7.  Select **Apply filter to database views and tables** to apply the filter to widgets based on both [database views](../../performance-analytics/concept/performance-analytics-glossary.md#) and tables.

    **Note:** It is not possible to apply filters to tables that extend the database view’s tables. For more information, see [Interactive filters on database views and table hierarchies](../../reporting/task/apply-filter-to-all-tables-in-hierarchy.md).

8.  In the **Date** section, use the slushbucket to select one or more date ranges that users can filter on.

    Available date filters are defined in the **Get Date Filter options for Date Filters** business rule. Customize this business rule to add or remove filter options.

9.  Select a **Default value** for the filter.

    This default is applied automatically for all users. Values that a user selects override the global default for that user. You can specify more than one default value when using a UI control type that enables multiple selections, such as **Select Multiple Input**.

    **Note:** To pass more than 50 default values, or if you see the error `This is exceeding the GET call limitation`, create multiple interactive filters.

10. Right-click on the form header and select **Save**.

11. In the **Interactive filter Dates** related list, select **New**.

12. In the **Table** field, select a table that has reports you want to filter.

13. In the **Field** field, select a date field to filter on.

14. Click **Submit**.


## What to do next

Repeat steps 8-11 as needed for each date field you want to filter on.

1.  After you create the filter, add it to a dashboard.
2.  On the dashboard, select the **Edit widget** icon \(![Edit columns icon](../image/icon-cogwheel-ac.png)\) on each visualization on the dashboard that should follow the filter and select **Follow interactive filter**.

**Parent Topic:**[Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md)

