---
title: Create a Boolean interactive filter
description: A Boolean interactive filter allows users to filter report widgets based on the value of a true/false field.
locale: en-US
release: australia
product: Interactive Filters
classification: interactive-filters
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Creating Interactive Filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a Boolean interactive filter

A Boolean interactive filter allows users to filter report widgets based on the value of a true/false field.

## Before you begin

Role required: hp\_publisher\_admin and report\_admin. The hp\_publisher\_admin role exists only for managing interactive filters in Core UI. By default, it contains the role analytics\_filter\_admin for managing Core UI filters that are migrated to Platform Analytics experience.

When a user selects `All`, they do not see a report with all filter options applied, they see the unfiltered report. This example of Boolean filter shows three options you can filter on: true, false, and All.

![Boolean filter example with the true option selected](../image/if-ex-bool.png)

**Note:** If the interactive filter has a default value or specifies the last selected value, non-responsive dashboards do not apply this value automatically. This feature is only available on [Responsive dashboards](../concept/c_ResponsiveDashboards.md).

## Procedure

1.  Check the existing interactive filters on the same table.

    1.  Navigate to **All** &gt; **Performance Analytics Administration** &gt; **Core UI Artifacts** &gt; **Interactive Filters** and select an interactive filter based on the same table you want to filter.

    2.  Under Related Links, select **Other filters on Table**.

    3.  Review the other filters that are available on the same table to see if the filter you want already exists.

2.  Navigate to **All** &gt; **Performance Analytics Administration** &gt; **Core UI Artifacts** &gt; **Interactive Filters**.

3.  Select **New**.

4.  In the **Filter based on** list, select **Boolean**.

    ![Filter based on list with Boolean selected](../../reporting/image/if-filter-based-on-bool.png)

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

8.  In the **Table** list, select the table that includes the true/false field to filter on.

9.  In the **Field** list, select the true/false field to filter on.

10. Select a **Default value** for the filter.

    This default is applied automatically for all users. If a user selects a different value, that value is saved as the user's default and overrides the global default.

11. Select **Submit**.


## What to do next

1.  After you create the filter, add it to a dashboard.
2.  On the dashboard, select the **Edit widget** icon \(![Edit columns icon](../image/icon-cogwheel-ac.png)\) on each visualization on the dashboard that should follow the filter and select **Follow interactive filter**.

**Parent Topic:**[Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md)

