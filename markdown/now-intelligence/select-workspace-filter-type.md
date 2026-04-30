---
title: Create or add a filter on an inline dashboard
description: Create a filter or select one from the filter library. When creating a filter, name it, and choose whether to create a single select, multiple select, date, or true/false filter.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# Create or add a filter on an inline dashboard

Create a filter or select one from the filter library. When creating a filter, name it, and choose whether to create a single select, multiple select, date, or true/false filter.

## Before you begin

Role required: dashboard\_admin, or you must be the dashboard owner or have had editing rights shared with you.

## Procedure

1.  Open **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Locate the dashboard in the dashboard library and open it for editing, as described in [Edit Platform Analytics dashboards](../../dashboards/task/edit-db-in-ac.md).

    If the dashboard is in the inline editor, you see an **Edit** button. If it is a technical dashboard, you see an **Edit in UI Builder** button. In the latter case, go to [Create a filter on a technical dashboard in UI Builder](add-filter-tech-dashboard.md).

3.  If you are in a different application scope than the dashboard, use the application picker to select the correct scope.

    ![Application scope picker](../image/app-scope-picker.png)

4.  Select **Edit** to enter edit mode.

5.  Select **Add new element**.

6.  Select **Filter** then either a new or a saved filter.

    -   Select **New filter** to create a filter from scratch.
    -   Select **Saved filter** to reuse a filter from the library.
    When you select **New filter**, the **Configuration** panel opens for the selected filter. When you select **Saved filter**, you can choose an existing filter to add to the dashboard.

7.  If you are creating a new filter, select the type of data to filter.

    Other configuration options vary depending on the data type you select. After you select the filter type, follow the instructions on the linked page to continue configuration.

    -   [Single select](create-select-filter-workspace.md): A single value from a set of choices. Single select is the default filter type.
    -   [Multiple select](create-select-filter-workspace.md): More than one value from a set of choices, such as both High and Critical Priority
    -   [Date](create-date-filter-workspace.md): A calendar date. You can also set a time. Automatically applies to all indicator data on page or tab.
    -   [True/False](create-boolean-filter-workspace.md): Whether a field value is true or false. Can also be used with indicator breakdowns that are based on a [bucket group](../../performance-analytics/concept/performance-analytics-glossary.md#) with only two values. The labels for 'true' and 'false' can be customized. The viewer can select **\(empty\)** to clear their selection.
8.  Choose the **Filter Element**.

    Element options depend on the filter type, but include Pill, Checkboxes, and Typeahead.

9.  In the **Filter label** field, type a meaningful name for the filter.

    This name is the name that the user sees.

10. Position the filter.

    If the dashboard has tabs, putting the filter in a tab affects only the visualizations in that tab. If the dashboard has no tabs, or you place the filter above the tabs, it affects all visualizations in the dashboard.


## What to do next

**Note:** Filter values persist across user sessions. When a viewer reopens a dashboard, whatever values they last selected for any filters on the dashboard are preselected. This feature applies only to dashboards created in the inline editor, not technical dashboards.

