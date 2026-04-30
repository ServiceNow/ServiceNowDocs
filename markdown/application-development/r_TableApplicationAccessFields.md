---
title: Table design and runtime settings
description: The Application access fields determine whether a table is accessible to other applications during design-time or run-time operations.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Table design and runtime settings

The Application access fields determine whether a table is accessible to other applications during design-time or run-time operations.

<table id="table_wyn_pzb_br"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Can read

</td><td>

Select the check box to allow script objects from other application scopes to read records stored in this table. This option offers runtime protection. For example, a script in another application can query data on this table. You must first select read access to grant any other API record operation.

</td></tr><tr><td>

Can write

</td><td>

Select the check box to allow script objects from other application scopes to modify records stored in this table. This option offers runtime protection. For example, a script in another application can modify a field value on this table. This option is available only when the **Can read** check box is selected.

 Clear the check box to prevent script objects from other application scopes from modifying data stored in this table.

</td></tr><tr><td>

Can create

</td><td>

Select the check box to allow script objects from other application scopes to create records in this table. This option offers runtime protection. For example, a script in another application can insert a new record in this table. This option is available only when the **Can read** check box is selected.

 Clear the check box to prevent script objects from other application scopes from creating records in this table.

</td></tr><tr><td>

Can delete

</td><td>

Select the check box to allow script objects from other application scopes to delete records from this table. This option offers runtime protection. For example, a script in another application can remove a record from this table. This option is available only when the **Can read** check box is selected.

 Clear the check box to prevent script objects from other application scopes from deleting records from this table.

</td></tr><tr><td>

Allow access to this table via web services

</td><td>

Select the check box to allow users to make inbound web service queries to this table. This option offers both design-time and runtime protection. The user performing the query must have the correct permissions to access this table, even when this check box is selected.

 Clear the check box to prevent users from making web service queries to this table.

</td></tr></tbody>
</table>-   **[Runtime access to applications tables](../concept/c_RuntimeAccessToAppTables.md)**  
Runtime access determines if an API or web service call can run against an application table.
-   **[Design-time access to application tables](../concept/c_DesignTimeAccessToAppTables.md)**  
As the application developer, you can grant or deny other applications the permission to create configuration records, also known as application files, that extend the functionality of an application.

**Parent Topic:**[Application access settings](../concept/c_ApplicationAccessSettings.md)

