---
title: Archiving records
description: Manage table size growth and improve query performance by archiving records.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manage data growth, Data Management, Tables and data, Configure core features, Administer]
---

# Archiving records

Manage table size growth and improve query performance by archiving records.

You can archive records in core tables such as the Task \[task\] table and records in custom tables that you create on the ServiceNow AI Platform using archive rules.

-   To archive Configuration Management Database \(CMDB\) CI records, use the CMDB Data Manager. See [Working with CMDB Data Manager](https://www.servicenow.com/docs/access?context=cmdb-data-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   To archive emails, activate the [Email retention](../../notification/concept/email-retention.md) plugin and use the archive and destruction rules that come with the plugin. Don’t use the archive feature to create your own archiving rules on the email table.

## Archive activation

When you activate an archive rule, the system performs the following actions:

-   Creates the archive table in the database. The archive table has the same name as the primary table with an "ar\_" prefix. For example, if you archive the Incident `[incident]` table, the archive table is `[ar_incident]`.
-   Stores an XML version of each archived record in the sys\_archive\_log table. This archive log is the same table for all archive rules, and you can’t alter this behavior. It’s also the only place where the sys\_id is stored together with the display value for reference fields.

    For example, for ar\_incident `<assigned_to>Fred Luddy</assigned_to>`, the sys\_archive\_log record is as follows:

    ```
    
    <assigned_to display_value="Fred Luddy">5137153cc611227c000bbd1bd8cd2005</assigned_to>
    ```

-   Converts multiple joined tables into a single flat-file archive table. The archive table no longer consists of a base table and extended tables.

    ![Conversion of Multiple Joined Tables into a Flat Archive Table](../../database-rotation/image/ConversionOfMultipleJoinedTablesIntoAFlatArchiveTable.png "Conversion of Multiple Joined Tables into a Flat Archive Table")

-   Converts reference field values \(values set by references to records in other tables\) into string values. The archive record contains the display value of the reference field at the time of the archive.
-   Adds a module to the **Archive Tables** list in the **System Archiving** application. The module name is a combination of the word "Archive" plus the display name for the archived table. For example, the archive module for the Attachment `[sys_attachments]` table is **Archive Attachment**.
-   Creates a list of the archive table using the default list view.
-   Creates a form for the archive table using the default form view. The form excludes any [dot-walking](https://www.servicenow.com/docs/access?context=c_DotWalking&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) fields such as **Caller ID.Email**.

## Reference values converted to strings

Archived data is stored as a flat file with no reference fields to other tables. The archive process converts any references to other tables to string values.

In the case of a reference field, the string uses the [display value](../../field-administration/concept/c_DisplayValues.md) such as the caller's user name. For example, the **Caller** reference field in an incident would display the string ITIL User. If the reference was a document ID and the archive rule included the option to archive related document IDs, the string is the document ID of the related record.

Future changes to reference values aren't reflected in archived records. For example, if you change the user name for "John Smith" to "John A Smith", all active incident records automatically show the caller as "John A Smith" because of the reference between the Incident and User tables. However, all archived incident records display the user name that existed at the time of the archive. Likewise, if you delete a user from the system, current incidents no longer display the deleted user as a caller. However, archived incidents still display the string "John Smith" because that value was used when the record was archived.

## Querying archived data

Archived tables aren’t optimized for ad hoc queries. They only contain index entries for the display value, creation date, and the primary key of sys\_id.

Avoid making on-demand queries against an archived table, like searching for all priority 1 archived incidents. Instead, only search against the indexed fields. For example, search for incident INC100001 or incidents created on a specific date.

## Archive tables and ACLs

By default, archive tables use the ACLs for the unarchived table of the same name. For example, the archived Incident `[ar_incident]` table uses the ACLs defined for the unarchived Incident `[incident]` table.

You can manage access to archive tables explicitly by creating ACLs for specific archive tables and setting the **glide.security.enable\_archive\_table\_acls** property to **true**. The system then follows one of two paths:

1.  If one or more active ACLs are defined for an archive table, those ACLs control access to the archive table.
2.  If no ACLs are defined for an archive table, the system reverts to default behavior and uses the ACLs for the unarchived version of the table.

**Note:** The two paths are mutually exclusive: If archive table ACLs deny access, the system doesn't attempt to revert to the default behavior.

The read operation is the only operation evaluated, and other operations are prevented.

The Execution Plan UI is aware of this logic and presents information accordingly. For example, adding the first ACL to an archive table shows that the archive table ACL is "masking" ACLs on the unarchived \(original data\) table.

If you have existing ACLs on archived tables, they’re ignored unless you set the **glide.security.enable\_archive\_table\_acls** property to **true**. Those newly activated ACLs may possibly cause access issues. To prevent this occurrence, the system sets the **glide.security.enable\_archive\_table\_acls** property as follows:

-   Instances without the **glide.security.enable\_archive\_table\_acls** property use the default value of **false**.
-   Upgraded instances don't install the property. The property must be added manually and set to **true** to enable the archive table ACL behavior.
-   Zbooted instances install the property and set it to **true**.

## Setting the language of archived strings

On internationalized instances, the archive process uses the language of the SYSTEM user to select the display value strings.

If there’s no SYSTEM user, the instance uses the default language setting to select the display value strings. You can either create a SYSTEM user with a specific language setting or set the system default language to [select the language of archived strings](../../localization/reference/r_GlobalLanguage.md).

-   **[Create an archive rule](../../database-rotation/task/t_CreateAnArchiveRule.md#)**  
Define the criteria for archiving records by creating an archive rule.
-   **[Archive related records](../../database-rotation/task/t_ArchiveRelatedRecords.md)**  
Archive, clear, or delete related records from an archive rule.
-   **[Managing archived data](managing-archived-data.md#)**  
Change the schedule for an archive rule, stop the archive rule from running, or restore your archived data.
-   **[Migrating non-reference fields to reference fields](../../database-rotation/reference/archive-reference-migration.md)**  
Manually preserve sys\_ids in reference fields instead of storing the display name as a string.

**Parent Topic:**[Managing the growth of data on your instance](data-management-policies.md)

