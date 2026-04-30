---
title: Viewing Sys Audit and Audit Relationship Change tables
description: The ServiceNow AI Platform tracks inserts and updates to audited records in the Sys Audit \(sys\_audit\) and Audit Relationship Change \(sys\_audit\_relation\) tables.The Sys Audit \[sys\_audit\] table tracks changes to reference fields in tables that are flagged for auditing. This activity includes journal field entries and history sets. The Audit Relationship Change \[sys\_audit\_relation\] table tracks relationship changes between sys\_audit table records and the source tables that the audited records originate from. It also tracks when a record might have been deleted.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Auditing]
---

# Viewing Sys Audit and Audit Relationship Change tables

The ServiceNow AI Platform tracks inserts and updates to audited records in the Sys Audit \(sys\_audit\) and Audit Relationship Change \(sys\_audit\_relation\) tables.

The ServiceNow AI Platform tracks audit tables. To track tables, select the **Audit** check box in the dictionary record to set the value to true. By default, it does not audit records from system tables, such as update sets tables.

**Note:** To prevent performance issues and infinite loops, the system skips any business rule or workflow triggered by inserts to the Sys Audit table.

## Sys audit table columns

Access the Sys Audit table on your instance by entering `sys_audit.list` in the navigation filter.

The following columns appear in the sys\_audit table records:

<table id="table_jbh_cj1_l1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name

</td><td>

Table that the audit record is for \(for example, "`incident`"\)

</td></tr><tr><td>

Field name

</td><td>

Column in the table that the audit record is for \(for example, "`assigned_to`"\)

</td></tr><tr><td>

Document key

</td><td>

Sys\_id \(Unique Record Identifier\) for the originating record associated with the audit record.

</td></tr><tr><td>

User

</td><td>

Name of the user who created the change.

 **Note:** Some automated processes use the system or guest user to apply and track changes to records. For more information, see [System and guest users](https://www.servicenow.com/docs/access?context=user&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US#system-guest-users).

</td></tr><tr><td>

Old value

</td><td>

Old value of the field change represented by this sys\_audit record.

 -   Reference fields: Unique sys\_id value of the changed record.
-   Date and time fields: Value in Coordinated Universal Time \(UTC\) as stored in the database.

</td></tr><tr><td>

New value

</td><td>

New value of the field change represented by this sys\_audit record.

 -   Reference fields: Unique sys\_id value of the changed record.
-   Date and time fields: Value in Coordinated Universal Time \(UTC\) as stored in the database.

</td></tr></tbody>
</table>## How the Audit Relationship Change \(sys\_audit\_relation\) table works

The Sys Audit \[sys\_audit\] table tracks changes to reference fields in tables that are flagged for auditing. This activity includes journal field entries and history sets. The Audit Relationship Change \[sys\_audit\_relation\] table tracks relationship changes between sys\_audit table records and the source tables that the audited records originate from. It also tracks when a record might have been deleted.

-   -   Whenever you audit any record in a table, a relationship is created between the various originating tables to the store that records data. This relationship information is saved in the sys\_history\_set, sys\_history\_line, and sys\_journal tables.
-   If you delete a field that is related to an audited table record, the sys\_audit\_relation table records the deletion. In other words, anytime you change an audited record, it first deletes past elements, and then creates a relationship in the sys\_audit\_relation table with new document IDs.

