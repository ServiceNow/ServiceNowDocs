---
title: Create an interactive filter for whether a field is empty or populated
description: You can create a Boolean interactive filter that lets users filter report widgets based on whether a specific field is empty or populated.
locale: en-US
release: australia
product: Interactive Filters
classification: interactive-filters
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating Interactive Filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create an interactive filter for whether a field is empty or populated

You can create a Boolean interactive filter that lets users filter report widgets based on whether a specific field is empty or populated.

## Before you begin

Role required: hp\_publisher\_admin and report\_admin. The hp\_publisher\_admin role exists only for managing interactive filters in Core UI. By default, it contains the role analytics\_filter\_admin for managing Core UI filters that are migrated to Platform Analytics experience.

**Note:** If the interactive filter has a default value or specifies the last selected value, non-responsive dashboards do not apply this value automatically. This feature is only available on [Responsive dashboards](../concept/c_ResponsiveDashboards.md).

## About this task

Create this filter for a field where **Yes** filters for records where the specified field is populated and **No** filters for records where the field is empty. Name the filter to represent this logical relationship. For example, you can use the name "Incident generated problem" for a filter based on the Incident table and the Problem field.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics Administration** &gt; **Core UI Artifacts** &gt; **Interactive Filters**.

2.  Select **New**.

3.  In the **Filter based on** list, select **Boolean**.

4.  Set the following fields:

    |Name|Description|
    |----|-----------|
    |Name|Enter a name for the filter. This name appears on the dashboard widget for the filter.|
    |Look up name|Enter a lookup name for the filter. This name appears in the **Add content** menu for users adding a filter to a dashboard. Use this name to help organize your filters. If you do not specify a lookup name, the **Name** value is used instead.|
    |Description|Enter a description of the filter.|
    |UI control type|Select how the available filtering options for this filter appear on the dashboard widget. See [Available interactive filter UI control types](../reference/r_HomepagePublisherUIControlTypes.md).|

5.  Select **Apply to all tables in hierarchy** to apply the filter to parent, child, and sibling tables of an extended table.

6.  Select **Apply filter to database views and tables** to apply the filter to widgets based on both [database views](../../performance-analytics/concept/performance-analytics-glossary.md#) and tables.

    **Note:** It is not possible to apply filters to tables that extend the database view’s tables. For more information, see [Interactive filters on database views and table hierarchies](../../reporting/task/apply-filter-to-all-tables-in-hierarchy.md).

7.  In the **Table** list, select the table that contains the field to filter on.

8.  In the **Field** list, select the field to filter on.

9.  Select **Submit**.


## What to do next

After you create the filter, add it to a dashboard.

**Parent Topic:**[Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md)

