---
title: Create a filter group
description: Create a set of filters that you can apply simultaneously. When you have multiple filters, applying them all together can be faster than applying them separately.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/create-filter-group.html
release: brazil
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 4
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# Create a filter group

Create a set of filters that you can apply simultaneously. When you have multiple filters, applying them all together can be faster than applying them separately.

## Before you begin

Role required: dashboard\_admin, or you must be the dashboard owner or have had editing rights shared with you.

## About this task

If you have many filters that apply to many visualizations on a dashboard, it can take a long time to apply all the filters. Each filter whose value you set makes a separate call to the ServiceNow AI Platform. You can speed this process up by organizing filters into groups, where you make a single call to apply multiple filters at the same time.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Locate and open or create the dashboard to which you want to add a filter group.

    Technical dashboards are not supported. You can only add a filter group to a dashboard in the inline editor. For more information, see [Edit Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/edit-db-in-ac.md).

3.  Select **Add new element** and add a Filter Group element.

4.  In the **UI Element** section, configure the appearance of the filter group.

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

    -   [Single select](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-select-filter-workspace.md): A single value from a set of choices. Single select is the default filter type.
    -   [Multiple select](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-select-filter-workspace.md): More than one value from a set of choices, such as both High and Critical Priority
    -   [Date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-date-filter-workspace.md): A calendar date. You can also set a time. Automatically applies to all indicator data on page or tab.
    -   [True/False](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-boolean-filter-workspace.md): Whether a field value is true or false. Can also be used with indicator breakdowns that are based on a [bucket group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) with only two values. The labels for 'true' and 'false' can be customized. The viewer can select **\(empty\)** to clear their selection.
    When you complete the configuration of each filter, select **Back to group configuration**.

6.  Configure any additional settings that you want to change.

<table id="table_k2b_xfh_xcc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show group apply

</td><td>

Turn on to enable applying all filters in the group together. When not selected, changes to any individual filters in the group apply immediately.Default: on

</td></tr><tr><td>

Show group clear

</td><td>

Turn on to enable clearing all filters in the group together.Default: on

</td></tr><tr><td>

Show group reset

</td><td>

Turn on to enable resetting all filters in the group to their default values together.Default: off

</td></tr><tr><td>

Combine clear and reset

</td><td>

Turn on to move Clear and Reset into a More actions \[Omitted image "icon-menu.png"\] Alt text: Menu icon menu.Available only when **Show group reset** is on.

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

\[Omitted image "filter-group-simple.gif"\] Alt text: Filters being set and cleared in a group.

