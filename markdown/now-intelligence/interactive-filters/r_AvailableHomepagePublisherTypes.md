---
title: Creating Interactive Filters of different types
description: You can create and configure Interactive Filters for multiple field types.
locale: en-US
release: zurich
product: Interactive Filters
classification: interactive-filters
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Creating Interactive Filters of different types

You can create and configure Interactive Filters for multiple field types.

Before you create an interactive filter, choose which type of filter to create.

<table id="table_ayz_zzg_kr"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Choice list](../task/t_CreateAChoiceListPublisher.md)

</td><td>

Allows you to filter data based on the value of a specific choice list. You must select the table and choice list field. The filter affects reports on the specified table.

</td></tr><tr><td>

[Reference](../task/t_CreateAReferenceFieldPublisher.md)

</td><td>

Allows you to filter data based on the value of one or more reference fields. You must select the referenced table, as well as reference fields from other tables. The filter affects reports on tables that have the specified reference fields.**Note:** Reference interactive filters do not support string fields.

</td></tr><tr><td>

[Date](../task/t_CreateADatePublisher.md)

</td><td>

Allows you to filter data based on the value of one or more date fields. You must select the tables and date fields. The filter affects reports on the specified tables.

</td></tr><tr><td>

[Boolean](../task/t_CreateABooleanPublisher.md)

</td><td>

Allows you to filter data based on the value in a specific true/false field. You must select the table and the true/false field. The filter affects reports on the specified table.

</td></tr><tr><td>

[Group](../task/t_CreateAGroupPublisher.md)

</td><td>

Allows you to display multiple interactive filters in a single widget on a dashboard. Users viewing the dashboard can select which grouped filters to apply.

</td></tr><tr><td>

[Empty/non-empty](../task/t_CreateAEmptyNonemptyFilter.md)

</td><td>

Filter based on whether a field contains a value.

</td></tr><tr><td>

[Cascading](../task/create-cascading-filter.md#)

</td><td>

Allow you to filter based on multiple values in a hierarchy, such as by region, country, and city.

</td></tr></tbody>
</table>-   **[Create a choice list interactive filter](../task/t_CreateAChoiceListPublisher.md)**  
A choice list interactive filter enables users to filter report widgets based on the value of a choice list.
-   **[Create a reference field interactive filter](../task/t_CreateAReferenceFieldPublisher.md)**  
A reference field interactive filter allows users to filter report widgets based on the value of a reference field.
-   **[Create a date interactive filter](../task/t_CreateADatePublisher.md)**  
A date interactive filter allows users to filter report widgets based on the value in a date field.
-   **[Create a Boolean interactive filter](../task/t_CreateABooleanPublisher.md)**  
A Boolean interactive filter allows users to filter report widgets based on the value of a true/false field.
-   **[Create a group interactive filter](../task/t_CreateAGroupPublisher.md)**  
A group interactive filter allows users to select multiple interactive filters to apply to reports on a dashboard.
-   **[Create an interactive filter for whether a field is empty or populated](../task/t_CreateAEmptyNonemptyFilter.md)**  
You can create a Boolean interactive filter that lets users filter report widgets based on whether a specific field is empty or populated.
-   **[Create a cascading filter](../task/create-cascading-filter.md#)**  
Cascading filters allow you to filter based on multiple values in a hierarchy, such as by region, country, and city. Lower-level choices are filtered by the values selected at higher levels.
-   **[Interactive filters on database views and table hierarchies](../../reporting/task/apply-filter-to-all-tables-in-hierarchy.md)**  
When you create an interactive filter on an extended table, you can also apply the filter to database views and to the other tables in the hierarchy. The hierarchy includes all parent, child, and sibling tables.
-   **[Available interactive filter UI control types](r_HomepagePublisherUIControlTypes.md)**  
The interactive filter **UI control type** field provides several options for displaying the filter.

**Parent Topic:**[Interactive Filters](../concept/c_HomepagePublishers.md)

