---
title: Filter on multiple string values
description: For a string field, you can create a filter that searches for multiple values by creating a comma-delimited list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/t\_FilteringOnMultipleStringValues.html
release: australia
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "CommaDelimitedFilter.png"\] Alt text: Comma-delimited filter

    Alternatively, for text or number fields, type your search options. Separate the options by commas or put each option on a separate line, and do not enclose the selections in brackets.

    \[Omitted image "MultipleStringValuesText.png"\] Alt text: Incident field is one of list of incidents separated by next line

3.  Click **Run** to filter the list.

    The filter conditions appear as a comma-delimited string at the top of the results list.

    \[Omitted image "CommaDelimitedFilter2.png"\] Alt text: Comma-delimited filter string


**Parent Topic:**[Filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_Filters.md)

**Related topics**  


[Create a filter in List]()

[Add related list conditions]()

[OR conditions]()

[Dynamic operators]()

