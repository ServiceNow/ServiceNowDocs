---
title: Create a filter in the Filter Designer
description: Create a Platform Analytics filter in the Filter Designer and add it to the library for reuse.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-10-02"
reading_time_minutes: 3
breadcrumb: [Filters, Platform Analytics]
---

# Create a filter in the Filter Designer

Create a Platform Analytics filter in the Filter Designer and add it to the library for reuse.

## Before you begin

**Note:** Filters that are saved to the filter library are not accessible in the technical editor \(UI Builder\).

Role required: analytics\_filter\_admin, admin

## Procedure

1.  To add a filter to the filter library, navigate to **Platform Analytics** &gt; **Library** &gt; **Filters** and select **New**.

    The Filter Designer opens.

2.  Select the type of data to filter.

    Other configuration options vary depending on the data type you select.

    -   [Single select](create-select-filter-workspace.md): A single value from a set of choices. Single select is the default filter type.
    -   [Multiple select](create-select-filter-workspace.md): More than one value from a set of choices, such as both High and Critical Priority
    -   [Date](create-date-filter-workspace.md): A calendar date. You can also set a time. Automatically applies to all indicator data on page or tab.
    -   [True/False](create-boolean-filter-workspace.md): Whether a field value is true or false. Can also be used with indicator breakdowns that are based on a [bucket group](../../performance-analytics/concept/performance-analytics-glossary.md#) with only two values.
3.  In the **Filter label** field, type a meaningful name for the filter.

    This name is the name that the runtime user sees.


## Result

Upon saving, the filter is saved to the library, where any user can add it to their dashboards.

**Parent Topic:**[Filters in Platform Analytics](../concept/interactive-filters-workspace.md)

**Related topics**  


[Create or add a filter on an inline dashboard](select-workspace-filter-type.md)

[Create a filter on a technical dashboard in UI Builder](add-filter-tech-dashboard.md)

[Make a data visualization act as a filter](make-dv-act-as-filter.md)

[Configure a Single/Multiple select or cascading filter](create-select-filter-workspace.md)

[Configure a True/False filter](create-boolean-filter-workspace.md)

[Configure a Date filter in the inline editor](create-date-filter-workspace.md)

[Create a domain filter](create-domain-filter.md#)

[Edit a Platform Analytics filter on a dashboard](edit-filters-configurable-workspaces.md)

[Troubleshoot breakdown filters](troubleshoot-breakdown-filters.md)

