---
title: Create a search source
description: Create a search source to define what records can be found in your search bar.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure search criteria, Global search for mobile, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a search source

Create a search source to define what records can be found in your search bar.

## Before you begin

Role required: admin

## About this task

In these steps, you create the search source to define what search results your users can see. Each search source consists of a table, and optional conditions. User will see results from the selected table, limited by the conditions you define in the search source. You could, for example, select the Incident \[incident\] table, and then create a condition so that only incidents in the open state appear in search results. You can define more than one search source for a search, so your users can find records from multiple tables that match their search input.

## Procedure

1.  In the filter navigator, enter `sys_search_source.list`.

2.  Click **New**.

3.  On the Search Source field, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|The name of your search source. Enter a name that includes the name of the table you intend to use to make the search source easy to identify.|
    |Application|The scoped application for the search source. This field is ready only and automatically contains the name of the current application.|
    |Table|The table for this search source.|
    |Conditions|Conditions under which a record from the selected table appears in search results. For example, if you select &lt;Active&gt;&lt;is&gt;&lt;true&gt;, only active records appear in your search results.|

    A search source configured for the User \[sys\_user\] table.![Search source for the User, sys_user, table example.](../image/example-search-source.png)

4.  Select **Save**.

5.  Repeat steps 1 through 4 to define additional sources for your search.

    Note that additional search sources can impact the performance of your searches.


**Parent Topic:**[Configure search criteria](../concept/sg-create-custom-search.md)

