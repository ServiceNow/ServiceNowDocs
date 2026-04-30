---
title: Create a filter in the Filter Designer
description: Create a Platform Analytics filter in the Filter Designer and add it to the library for reuse.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
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

