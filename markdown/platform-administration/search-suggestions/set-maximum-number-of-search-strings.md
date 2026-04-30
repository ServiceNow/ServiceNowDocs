---
title: Set maximum age for searches used in suggestion generation
description: Set the Auto Flush parameter to limit the age of search strings used to create auto-complete suggestions and search suggestions.
locale: en-US
release: zurich
product: Search Suggestions
classification: search-suggestions
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Configuring Search Suggestions, Search Suggestions, Search administration, Configure core features, Administer]
---

# Set maximum age for searches used in suggestion generation

Set the Auto Flush parameter to limit the age of search strings used to create auto-complete suggestions and search suggestions.

## Before you begin

Role required: ais\_admin

## About this task

The Search Event \[sys\_search\_event\] table contains all of the strings used in searches. Scripts use this table to generate search analytics, search suggestions, and auto-complete suggestions. A system property sets the maximum age for records preserved in the table. The default is 180 days, but you can change this number to preserve search events for a shorter or longer duration. Longer durations increase the size of the table and its disk consumption.

## Procedure

1.  Navigate to the Auto Flush \[sys\_auto\_flush\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_auto_flush.list`.

    3.  Press Enter.

2.  Search on `*search` and open the **sys\_search\_event** record.

3.  On the Auto Flush form, edit the **Age in seconds** value.

    The default is 15,552,000 seconds, which is 180 days.


