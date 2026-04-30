---
title: Dictionary overrides
description: Dictionary overrides provide the ability to define a field on an extended table differently from the field on the parent table.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer]
---

# Dictionary overrides

Dictionary overrides provide the ability to define a field on an extended table differently from the field on the parent table.

For example, for a field on the Task \[task\] table, a dictionary override can change the default value on the Incident \[incident\] table without affecting the default value on Task \[task\] or on Change \[change\].

Administrators can override these aspects of a field:

-   Reference qualifiers
-   Dictionary attributes
-   Default values
-   Calculations
-   Field dependencies
-   Default column display values
-   Mandatory and read-only status

-   **[Define a dictionary override](../task/t_DefineADictionaryOverride.md)**  
Use a dictionary override to allow a field in a child table to have a different value or behavior than the same field in a parent table. For example, a dictionary override changes the default value of the priority field from 4 in the parent table to 5 in the Incident table.

**Parent Topic:**[Managing tables and indexes](../../table-administration/concept/using-table-administration.md)

