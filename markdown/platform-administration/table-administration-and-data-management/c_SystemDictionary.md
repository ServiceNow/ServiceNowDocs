---
title: System dictionary
description: View a list of all tables in columns in your instance from the system dictionary.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring tables, Table admin, Tables and data, Configure core features, Administer]
---

# System dictionary

View a list of all tables in columns in your instance from the system dictionary.

Each row in the system dictionary represents either a table or a column in one of the tables. The system dictionary provides options for administrators to modify tables and fields, which in turn define lists and forms.

Use caution when changing system dictionary records because changes can have a high impact on functionality. In particular, changes to dictionary entries for system tables, which are tables that begin with sys\_, can create system-wide issues such as the inability to use update sets.

Dictionary changes are difficult to reverse. Also, dictionary changes automatically apply to all extended tables unless a dictionary override is defined. Be sure that changes are well-tested before applying them to a production instance.

## Creation options

When you create a field from the system dictionary, it is automatically added at the end of the first section of the default form view.

In most cases, use the following interfaces rather than creating entries directly on the system dictionary:

-   To create tables and fields, use the Tables module.
-   To create fields, configure the table form.

**Parent Topic:**[Exploring ServiceNow AI Platform tables](../../table-administration/concept/exploring-table-administration.md)

