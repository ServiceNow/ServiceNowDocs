---
title: Filter on multiple string values
description: For a string field, you can create a filter that searches for multiple values by creating a comma-delimited list.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Filters, Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Filter on multiple string values

For a string field, you can create a filter that searches for multiple values by creating a comma-delimited list.

## Before you begin

Role required: admin

## About this task

This feature enables administrators to copy and paste search criteria from a Microsoft Excel spreadsheet into a filter, for example.

**Note:** Do not use the **\[is one of\]** operator on fields that contain commas, as the query does not return the expected set of records. Instead, create a filter using multiple **\[or\]** statements.

## Procedure

1.  Create the filter with the **\[is one of\]** or **\[is not one of\]** operator.

    Depending on the selected field, a choice list or a text box appears.

2.  Select one or more of the options by using multiple selection key commands.

    The choice list remains visible.

    ![Comma-delimited filter](../image/CommaDelimitedFilter.png)

    Alternatively, for text or number fields, type your search options. Separate the options by commas or put each option on a separate line, and do not enclose the selections in brackets.

    ![Incident field is one of list of incidents separated by next line](../image/MultipleStringValuesText.png)

3.  Click **Run** to filter the list.

    The filter conditions appear as a comma-delimited string at the top of the results list.

    ![Comma-delimited filter string](../image/CommaDelimitedFilter2.png "Comma-delimited filter string")


**Parent Topic:**[Filters](../concept/c_Filters.md)

**Related topics**  


[Create a filter in List](t_CreatingFilters.md)

[Add related list conditions](../../using-lists-v3/task/create-related-list-query.md)

[OR conditions](../concept/c_UsingORConditions.md)

[Dynamic operators](../reference/r_UsingTheDynamicOperator.md)

