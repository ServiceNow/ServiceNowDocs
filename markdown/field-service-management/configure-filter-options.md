---
title: Configure resource filter options
description: Administrators can configure more options for dispatchers to create advanced resource filters with beyond the default options.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced resource filters, Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure resource filter options

Administrators can configure more options for dispatchers to create advanced resource filters with beyond the default options.

## Before you begin

Role required: admin

## About this task

By default, dispatchers can create advanced filters based off of:

-   Username or user skill in the **Agents** tab.
-   Crew name or crew skill in the **Crews** tab.
-   Equipment category or resource type in the **Equipment** tab.
-   Contractor name in the **Contractor** tab.

    **Note:** In the **Contractor** tab the field that you select to filter a contractor is labeled Assignment Group, even though you are filtering on contractors.


You can also extend any table related to users or crews and use the fields from those tables to create resource filters. For more information, see [Configuring advanced resource filters for Dispatcher Workspace](../concept/configure-advanced-filter.md).

## Procedure

1.  Choose one of the following:

    -   Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace Configuration** &gt; **Agent Filter Configuration**.
    -   Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace Configuration** &gt; **Crew Filter Configuration**.
    -   Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace Configuration** &gt; **Equipment Filter Configuration**.
    -   Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace Configuration** &gt; **Contractor Filter Configuration**.
    -   If you extended a table, navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace Configuration** and then select the table you extended.
2.  Select one of the tables.

    For a list of tables, see [Advanced resource filter tables](../reference/advanced-filter-tables.md).

3.  Select **New**.

4.  Select the **Field** that dispatchers will be able to use as the new search value.

5.  Select **Submit**.

    Dispatchers can now create advanced resource filters using the value you chose in step 4.


