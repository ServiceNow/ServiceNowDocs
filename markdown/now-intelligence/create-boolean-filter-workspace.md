---
title: Configure a True/False filter
description: Let users filter on true/false fields and breakdown elements. For example, you can enable users to choose only the incidents where the Active field is set to true.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# Configure a True/False filter

Let users filter on true/false fields and breakdown elements. For example, you can enable users to choose only the incidents where the **Active** field is set to **true**.

## Before you begin

**Important:** This procedure assumes you’ve created a filter in the Filter designer or added a filter to your dashboard with the True/False filter type. For more information, see [Create or add a filter on an inline dashboard](select-workspace-filter-type.md) or [Create a filter in the Filter Designer](add-filter-library.md).

Role required: In the dashboard inline editor: dashboard\_admin, or you must be the dashboard owner or have had editing rights shared with you.

In the Filter Designer \(**Library** &gt; **Filters** &gt; **New**\): analytics\_filter\_admin, admin

## About this task

The filter applies to all elements on the same dashboard or the same dashboard tab, depending on filter placement.

## Procedure

1.  Create a filter and select the True/False filter type, as described in [Create or add a filter on an inline dashboard](select-workspace-filter-type.md) or [Create a filter in the Filter Designer](add-filter-library.md).

2.  Set custom display labels in place of 'True' and 'False,' such as 'Yes' and 'No.'

3.  In **Data to filter**, specify a table field, indicator breakdown, or Usage Insights property to filter.

    You can add any number of targets to the filter. Select either a table and field or all indicators with a particular breakdown. If you select a table, you can also select to apply the filter to the hierarchy of related tables: Parents, children, siblings, and any [database views](../../performance-analytics/concept/performance-analytics-glossary.md#) that contain the table.

    MetricBase and Workflow Data Fabric tables can be filtered, and are listed with the other tables.

    **Note:**

    -   If you select a table, you must select at least one true/false \(Boolean\) field. You can only select true/false fields.
    -   To help you select only true/false indicator breakdowns, your choice is limited to breakdowns based on a bucket \[pa\_buckets\] with only two values. However, the system can’t check whether the indicator breakdown is really true/false. You have to determine whether the breakdown is Boolean yourself. Ask your ServiceNow AI Platform administrator for help.
    -   An empty \(null\) value is possible for a field. Therefore, the total number of true and false values can be less than the total number of records or less than an indicator score that counts records. The viewer can also select **\(empty\)** to clear their selection.
4.  Specify a default value of true or false.

    The filter is applied with this value when the dashboard is opened. If you do not specify a default value, the filter value is empty by default.

5.  Select the **Sort direction**.

    If you select **Ascending**, the lowest filtered values are shown first. If you select **Descending**, the highest values are shown first. The user can change this value.

6.  Select **Save**.


## Result

The filter is ready to use when you exit editing mode.

## What to do next

If you have the required roles, add the filter to the filter library. You can also reconfigure, delete, or duplicate the filter. For more information, see [Edit a Platform Analytics filter on a dashboard](edit-filters-configurable-workspaces.md).

**Related topics**  


[Applying filters to Process Mining maps](../concept/applying-filters-to-process-optimization-maps.md)

[Edit a Platform Analytics filter on a dashboard](edit-filters-configurable-workspaces.md)

[Configure a data visualization to follow filters or not](configure-dv-follow-filters-or-not.md)

