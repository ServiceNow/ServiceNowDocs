---
title: Create a record hierarchy
description: Build a record hierarchy between records in the same table.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building hierarchical queries, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a record hierarchy

Build a record hierarchy between records in the same table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Record Hierarchy**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Label used for displaying the record hierarchy.|
    |Name|Internal name for the record hierarchy.|
    |Table|The table with records that you want organize into a hierarchy.|
    |Reference Field|The self-reference field that defines parent-child relationships between records in the selected table.|

4.  Select **Submit**.


## Result

A record hierarchy based on the specified reference field is created. The ServiceNow AI Platform automatically builds the hierarchy paths that define the relationships between records in the hierarchy.

## What to do next

Build queries in condition builder using the \[is in hierarchy\] or \[is in hierarchy \(dynamic\)\] operators. See [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

