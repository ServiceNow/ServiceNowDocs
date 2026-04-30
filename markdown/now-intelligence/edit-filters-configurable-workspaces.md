---
title: Edit a Platform Analytics filter on a dashboard
description: When you highlight a filter on a dashboard that you have put into edit mode, you have several editing options depending on whether the filter is local to the dashboard or saved in the library.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# Edit a Platform Analytics filter on a dashboard

When you highlight a filter on a dashboard that you have put into edit mode, you have several editing options depending on whether the filter is local to the dashboard or saved in the library.

## Before you begin

Role required: dashboard\_admin, or you must be the dashboard owner or have had editing rights shared with you.

## About this task

**Note:** This topic covers only those editing options you have in the component header on a filter on a dashboard that is in editing mode. It does not cover the configuration options, such as selecting the filter source and target. Those options are available in the configuration panel, which is available in either a dashboard in edit mode or in the Filter Designer. The editing options in this topic apply to all filter types, whereas the configuration options differ by filter type. For more information, see [Configure a Single/Multiple select or cascading filter](create-select-filter-workspace.md), [Configure a True/False filter](create-boolean-filter-workspace.md), or [Configure a Date filter in the inline editor](create-date-filter-workspace.md).

## Procedure

1.  Navigate to the dashboard with the filter that you want to edit.

2.  Select **Edit** to put the dashboard in edit mode.

3.  Select the filter that you want to edit.

    A border around the filter appears with various information and options.

    ![Options for filter that exists only on the dashboard.](../image/filter-db-local-options.png "Options for a filter that is local to the dashboard")

    ![Options for a filter included from the filter library.](../image/filter-db-shared-options.png "Options for a saved filter from the library") ![]( "Options for a saved filter from the library")

    -   Filter \| Saved filter: Shows whether the filter exists only locally in the dashboard or is a filter that is saved in the filter library. Options between the two filters differ.
    -   Resize: Lets you drag the corners of a filter to resize it. Also lets you add other components around the filter.
    -   Configure: Opens the filter in the Configuration panel, if it is not already open.

        **Warning:** You need the viz\_admin role or higher to edit a saved filter in a dashboard. If you do not have this role, you see a warning that you cannot configure the element. If you have the analytics\_filter\_admin role or higher \(dashboard\_admin\), you can open the filter for editing from the Filter library. Alternatively, you can select **Unlink from library** to convert the filter to a local version that exists only on the dashboard.

        For more information about configuring the filter, see one of the following topics:

        -   [Configure a Single/Multiple select or cascading filter](create-select-filter-workspace.md)
        -   [Configure a Date filter in the inline editor](create-date-filter-workspace.md)
        -   [Configure a True/False filter](create-boolean-filter-workspace.md)
4.  Expand the **Actions** \(![More action icon](../image/icon-paw-more-actions.png)\) menu and select from the following actions, which are different for local and saved filters:

    |Action|Description|
    |------|-----------|
    |Add to library|Adds the filter to the filter library so that any user can use it on other dashboards. Requires the analytics\_filter\_admin role.|
    |Duplicate|Makes a copy of the filter on the same dashboard for you to edit.|
    |Open record|Opens a form so that you can examine and edit the filter's JSON code. Requires the admin role.|
    |Delete|Removes the filter from the dashboard.|

    |Action|Description|
    |------|-----------|
    |Edit in Designer|Opens the filter outside of the dashboard in the Filter designer for configuration. Requires the viz\_admin role.|
    |Unlink from library|Replaces the saved filter with an identical filter that exists only on this dashboard. The original filter remains in the library and on any other dashboards. Only dashboard editing rights are required to edit this local version.|
    |Duplicate|Makes a copy of the current filter on both the same dashboard and in the library. Requires the viz\_admin role.|
    |Open record|Opens a form so that you can examine and edit the filter's JSON code. Requires the admin role.|
    |Delete|Removes the filter from the dashboard. It remains in the library and on other dashboards.|

5.  Select **Save** to save your changes and continue editing or select **Exit editing mode** to finish editing.

    When you save changes to a shared filter, you have two choices:

    -   Save the changes only for the current dashboard.

        This action creates a new version of the filter, like the **Unlink from library** action. The version of the filter in the library doesn’t change.

    -   Save changes to the library.

        When you make this selection, the new version of the filter is enabled on all dashboards that use it.


