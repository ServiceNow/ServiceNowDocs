---
title: Column filters in list components
description: If column filters are activated, viewers of a List can filter the list by the contents of individual columns. Filter options depend on the column type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/column-filters-in-lists.html
release: zurich
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 2
breadcrumb: [List visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Column filters in list components

If column filters are activated, viewers of a List can filter the list by the contents of individual columns. Filter options depend on the column type.

If column filtering is turned on for a List component, viewers of the list see an icon at the beginning of the filter columns. The exact position depends on localization. Select the icon to show or hide column filters.

\[Omitted image "show-list-column-filters.gif"\] Alt text: Showing and hiding column filters on a list.

**Note:** To turn on column filtering, a permitted user must activate **Show column filtering** in the List configuration panel. For more information, see [Create a list visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-dv-analytics-list.md).

Column filters differ from the filters you can select when you select the data source for a List in two important ways:

-   To configure a column filter, you only need the right to read the List. Filters on the data source require the right to configure the List.
-   Because of the relaxed access, column filters apply only in the session in which they are set. Filters on the data source persist and apply to all viewers of the List.

The available filters fall into several types:

-   **Filter by value**

    Field classes: Most string and numeric classes

    First you choose an operator such as "is" or "contains." Then you type in a value, such as "SAP."

    \[Omitted image "column-filter-value.png"\] Alt text: Filtering the Description field on text that contains "SAP."

-   **Filter by date**

    Field classes: Date/time

    For a date/time field, you choose an operator like "on" or "before." Then you select a calendar date and possibly a time.

    \[Omitted image "column-filter-date.png"\] Alt text: Filtering the Activity due field by the date due \("on" operator\).

-   **Filter by choice value**

    Field classes: Choice

    Select one or more choices to filter by.

    \[Omitted image "column-filter-choce.png"\] Alt text: Filtering by values of the State field.

-   **Filter by condition builder in panel**

    Field classes: related\_tags, glide\_list, password, currency2, user\_image

    Some complex fields require you to build a condition to filter them by. For these fields, you open a panel, then use a standard condition builder. You can include related list conditions. You can add or edit filters on other columns in the list. For example, you could open a filter panel on the Indicator.Work notes list field and add a filter to the Description field.

    \[Omitted image "column-filter-panel.png"\] Alt text: Panel opened for the Work notes list field, showing conditions for the Work notes list and Description fields.


**Parent Topic:**[Create a list visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-dv-analytics-list.md)

**Related topics**  


[Create a list visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/create-dv-analytics-list.md)

[Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/c_ConditionBuilder.md)

[Create a filter in List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/t_CreatingFilters.md)

[Add related list conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/create-related-list-query.md)

