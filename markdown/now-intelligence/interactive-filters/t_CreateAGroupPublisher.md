---
title: Create a group interactive filter
description: A group interactive filter allows users to select multiple interactive filters to apply to reports on a dashboard.
locale: en-US
release: xanadu
product: Interactive Filters
classification: interactive-filters
topic_type: task
last_updated: "2026-01-08"
reading_time_minutes: 2
breadcrumb: [Creating Interactive Filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a group interactive filter

A group interactive filter allows users to select multiple interactive filters to apply to reports on a dashboard.

## Before you begin

Role required: hp\_publisher\_admin and report\_admin. The hp\_publisher\_admin role exists only for managing interactive filters in Core UI. By default, it contains the role analytics\_filter\_admin for managing Core UI filters that are migrated to Platform Analytics experience.

**Note:** If the interactive filter has a default value or specifies the last selected value, non-responsive dashboards do not apply this value automatically. This feature is only available on [Responsive dashboards](../concept/c_ResponsiveDashboards.md).

Before starting this procedure, create several choice list, reference field, boolean, or date filters to group.

Default values selected for child filters are not applied when using a group filter. Selected values in a group filter are not saved when you reload the dashboard.

## Procedure

1.  Check the existing interactive filters on the same table.

    1.  Navigate to **sys\_ui\_hp\_publisher.list** and select an interactive filter based on the same table you want to filter.

    2.  Under Related Links, select **Other filters on Table**.

    3.  Review the other filters that are available on the same table to see if the filter you want already exists.

2.  Navigate to **sys\_ui\_hp\_publisher.list**.

3.  Select **New**.

4.  In the **Filter based on** list, select **Group**.

    ![Filter based on list with Group selected](../../reporting/image/if-filter-based-on-group.png)

5.  Set the following fields:

    |Name|Description|
    |----|-----------|
    |Name|Enter a name for the filter. This name appears on the dashboard widget for the filter.|
    |Look up name|Enter a lookup name for the filter. This name appears in the **Add content** menu for users adding a filter to a dashboard. Use this name to help organize your filters. If you do not specify a lookup name, the **Name** value is used instead.|
    |Description|Enter a description of the filter.|

6.  In the **Group** section, select **Insert a new row**.

7.  Select an interactive filter to add to this group.

    You cannot add a group filter to another group filter.

8.  Repeat the previous two steps as needed for each filter you want to group.

9.  Click **Submit**.


## What to do next

1.  After you create the filter, add it to a dashboard.
2.  On the dashboard, select the **Edit widget** icon \(![Edit columns icon](../image/icon-cogwheel-ac.png)\) on each visualization on the dashboard that should follow the filter and select **Follow interactive filter**.

**Parent Topic:**[Creating Interactive Filters of different types](../reference/r_AvailableHomepagePublisherTypes.md)

