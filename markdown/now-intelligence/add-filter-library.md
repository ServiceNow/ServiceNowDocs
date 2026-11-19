---
title: Create a filter in the Filter Designer
description: Create a Platform Analytics filter in the Filter Designer and add it to the library for reuse.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/add-filter-library.html
release: zurich
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 2
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# Create a filter in the Filter Designer

Create a Platform Analytics filter in the Filter Designer and add it to the library for reuse.

## Before you begin

**Note:** Filters that are saved to the filter library aren't accessible in the technical editor or other UI Builder pages.

Role required: analytics\_filter\_admin, admin

## Procedure

1.  To add a filter to the filter library, navigate to **Platform Analytics** &gt; **Library** &gt; **Filters** and select **New**.

    You can also navigate to this library from other Platform Analytics library pages.

    The Filter Designer opens.

2.  Select the type of data to filter.

    Other configuration options vary depending on the data type you select.

    -   [Single select](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-select-filter-workspace.md): A single value from a set of choices. Single select is the default filter type.
    -   [Multiple select](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-select-filter-workspace.md): More than one value from a set of choices, such as both High and Critical Priority
    -   [Date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-date-filter-workspace.md): A calendar date. You can also set a time. Automatically applies to all indicator data on page or tab.
    -   [True/False](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-boolean-filter-workspace.md): Whether a field value is true or false. Can also be used with indicator breakdowns that are based on a [bucket group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md) with only two values. The labels for 'true' and 'false' can be customized. The viewer can select **\(empty\)** to clear their selection.
3.  Choose the **Filter Element**.

    Element options depend on the filter type, but include Pill, Checkboxes, and Typeahead.

4.  In the **Filter label** field, type a meaningful name for the filter.

    This name is the name that the user sees.

5.  Complete the settings that are specific to the filter type you selected.

    |Filter type|Instructions|
    |-----------|------------|
    |**Single select or Multiple select**|[Configure a Single/Multiple select or cascading filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-select-filter-workspace.md)|
    |**Date**|[Configure a Date filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-date-filter-workspace.md)|
    |**True/False**|[Configure a True/False filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-boolean-filter-workspace.md)|

6.  Select **Save**.


## Result

On saving, the filter is saved to the library, where any user can add it to their dashboards.

