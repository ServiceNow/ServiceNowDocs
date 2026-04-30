---
title: Create a filter group
description: Create a set of filters that you can apply simultaneously. When you have multiple filters, applying them all together can be faster than applying them separately.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# Create a filter group

Create a set of filters that you can apply simultaneously. When you have multiple filters, applying them all together can be faster than applying them separately.

## Before you begin

Role required: dashboard\_admin, or any role if you are the dashboard owner or have had editing rights shared with you.

## About this task

If you have many filters that apply to many visualizations on a dashboard, it can take a long time to apply all the filters. Each filter whose value you set makes a separate call to the ServiceNow AI Platform. You can speed this process up by organizing filters into groups, where you make a single call to apply multiple filters at once.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Dashboards**.

2.  Locate and open or create the dashboard to which you want to add a filter group.

    Technical dashboards are not supported. You can only add a filter group to a dashboard in the inline editor. For more information, see [Edit Platform Analytics dashboards](../../dashboards/task/edit-db-in-ac.md).

3.  Select **Add new element** and add a Filter Group element.

4.  In the **UI Element** section, configure the appearance of the filter group

<table id="table_odb_qdh_xcc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show filter group label

</td><td>

Turn on to show the label of the filter group.Default: on

</td></tr><tr><td>

Filter group label

</td><td>

A meaningful name for the filter group, which is visible to the user. Available only when **Show filter group label** is on.Default: Label

</td></tr><tr><td>

Filter group layout

</td><td>

Select Horizontal to show the filters side by side. Select Vertical to show the filters in a column.Default: Horizontal

</td></tr><tr><td>

Filter spacing

</td><td>

Choose how far apart you want to space the filters.Options: S, M, L

Default: S

</td></tr><tr><td>

Show values in pill

</td><td>

Turn on to show the selected filter elements inside the pill for all filters in the group.Default: on

</td></tr><tr><td>

Show border

</td><td>

Turn on to display a line around the filter group.Default: on

</td></tr><tr><td>

Bare

</td><td>

Turn on to remove padding around the filter group to provide more compact positioning. Available only when **Show border** is off.Default: off

</td></tr><tr><td>

Show round corners

</td><td>

Turn on to have the group border and radius match the pill border and radius. Available only when **Show values in pill** is turned off and **Show border** is turned on.Default: off

</td></tr></tbody>
</table>5.  Add filters.

    You can add filters of any type except Domain. The filter configuration is the same as for the Filter component:

    -   [Configure a Single/Multiple select or cascading filter](create-select-filter-workspace.md)
    -   [Configure a True/False filter](create-boolean-filter-workspace.md)
    -   [Configure a Date filter in the inline editor](create-date-filter-workspace.md)
    When you complete the configuration of each filter, select **Back to group configuration**.

6.  Configure any additional settings that you want to change.

<table id="table_k2b_xfh_xcc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show group apply

</td><td>

Turn on to enable applying all filters in the group together. When disabled, changes to any individual filters in the group apply immediately.Default: on

</td></tr><tr><td>

Show group clear

</td><td>

Turn on to enable clearing all filters in the group together.Default: on

</td></tr><tr><td>

Show group reset

</td><td>

Turn on to enable clearing all filters in the group together.Default: off

</td></tr><tr><td>

Combine clear and reset

</td><td>

Turn on to move Clear and Reset into a More actions ![Menu icon](../../../common/image/icon-menu.png) menu.Available only when **Show group reset** is on.

</td></tr><tr><td>

Show separator

</td><td>

Turn on to show a line between the filters and other content on the dashboard.Default: on

</td></tr><tr><td>

Max filter item width, px

</td><td>

Defines number of pixels allowed for each filter in the group. Text that is wider than this limit wraps to a new line.

</td></tr></tbody>
</table>
## Filter group in action

The following example shows a group of two filters being applied to a data visualization. A simple use case is used here for clarity and brevity. In practice, you would use a filter group with multiple visualizations and filters.

![Filters being set and cleared in a group.](../image/filter-group-simple.gif "Simple filter group")

