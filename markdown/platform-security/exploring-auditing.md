---
title: Exploring Auditing
description: Track record changes on auditing-enabled tables. By default, the system tracks changes to the incident, change, and problem tables, among others.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Auditing, Platform Security]
---

# Exploring Auditing

Track record changes on auditing-enabled tables. By default, the system tracks changes to the incident, change, and problem tables, among others.

Enabling auditing tracks the creation, update, and deletion of all records in the table. If you want to audit individual fields in a table, you can hide fields you don’t want to track using a dictionary attribute.

Auditing information is kept in these tables:

-   The [Audit](../../security/concept/c_UnderstandingTheSysAuditTable.md#) table.
-   The [Knowing about History sets](../../security/concept/c_HistorySets.md) table.

**Warning:** Auditing system tables that receive a large amount of traffic, such as workflow Contexts \[wf\_context\] or Event Management Alerts \[em\_alert\], can impact performance. For this reason, you can’t audit the em\_alert table as a whole. Instead, audit selected fields of interest. Set **audit=true** on both the em\_alert table and the selected fields. Try to audit as few fields as possible.

## Auditing parent and child tables

Tables don’t derive the audit flags from parent or child audited tables.

-   For example, if you enable auditing for the Configuration Items \[cmdb\_ci\] table, only CIs stored in that base table are audited.
-   Likewise, if you enable auditing for the Computers \[cmdb\_ci\_computer\] table, only the computer CI records are audited, including any fields on the Computers \[cmdb\_ci\_computer\] table that is derived from the Configuration Items \[cmdb\_ci\] table.

## Auditing system tables

By default, the system doesn’t audit the deletion of a record from system tables. To audit a system table, add it to the list of tables in the **glide.ui.audit\_deleted\_tables** property list.

## Auditing deletions from a form or list

By default, the system audits deletions of individual records from a form. To prevent auditing, set the table's dictionary attribute **no\_audit\_delete**.

The system audits deletions from a list when it **audit** is selected on the table dictionary, and the table isn’t listed in the **glide.db.audit.ignore.delete** property.

**Note:** By default, the **glide.db.audit.ignore.delete** property isn’t present in the System Property \[sys\_properties\] table. To change the property, and its associated values, you must first manually add it. However, when manually added, it overwrites the following default values:

`glide.db.audit.ignore.delete = sys_mutex,sys_db_cache,sys_lucene_block,sys_lucene_file,sys_lucene_directory,sys_user_preference,sys_audit,sc_cart,sc_cart_item,sys_trigger,wf_context,wf_activity,wf_condition,wf_executing,wf_history,wf_log,wf_transition,wf_transition_history, cmdb_ci_windows_service, cmdb_sam_sw_install, cmdb_software_instance, cmdb_sam_sw_usage, sam_sw_counter_detail`

To learn more about adding system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

It is to be noted that by default, the audit deletes are enabled whether the record is deleted from the form view, list view, or through a script/scheduled job.

## Information audited

Auditing tracks the following record changes:

-   Unique Record Identifier \(sys\_id\) of the record that changed
-   Field that changed
-   New field value
-   Old field value
-   Number of times this record and field have been updated
-   Date and time when the change occurred
-   User who made the change
-   Reason for the change \(if any reason is associated with the change\)
-   Internal checkpoint ID for the record, if the record has multiple versions.

## Information exempted from auditing

Some updates aren’t audited despite enabling auditing on a table. For example, you may see 132 updates in a record's history, but only seven audited ones.

Auditing excludes the following information:

-   Updates made by an upgrade.
-   Updates are made through import sets.
-   Records in parent or child tables.
-   Fields with the no\_audit dictionary attribute.
-   System tables are not listed in the **glide.ui.audit\_deleted\_tables** property list.
-   Fields that begin with the sys\_ prefix \(system fields\), except the sys\_class\_name and sys\_domain\_id columns.
-   UI Pages can sometimes trigger updates to a record without creating an audit log.
-   Anytime an inactivity monitor touches a record. It prevents you seeing possibly hundreds of updates listed against an incident, with the noise drowning out the useful data.
-   Manual changes to Performance Analytics scores.
-   Applying Update Set
-   Import XML

## Auditing a table

For instructions on how to audit a table, see [Configuring auditing for a table](../../security/task/t_EnableAuditingForATable.md).

By default, the system tracks all fields in an audited table. You can audit a subset of fields in a table in one of two ways:

-   You can enable auditing for the entire table, then exclude those fields you don’t want to include. It’s appropriate when you want to audit most, but not all, fields, and is referred to as an exclusion listing. For more information, see [Excluding a field from being audited \(exclusion listing\)](../../security/task/t_ExcludeAFieldFromBeingAudited.md).
-   You can enable auditing for the table, but only for specified fields. It’s appropriate when you want to audit only a small number of the table's fields and is referred to as an inclusion listing. For information on how to include a field using an inclusion listing, see [Including a table field in auditing \(inclusion listing\)](../../security/task/security-whitelist-audit-field.md).

## Non-cancellable audit records

Reduce the chances of audit records not being recorded when a transaction is canceled with the new default setting.

Audits have been set to create a record immediately in the same transaction with the target record write operations. If the target record gets deleted, the audit still gets created and retained under **NCA Test Audit Delete** module.

**Note:** The enhanced audit process is enabled by default. If the `glide.db.audit.lazy`property is set to `True`, the enhanced audit process is disabled.

Prior to Xanadu release, if a transaction is cancelled, certain auditable operations were missed being recorded. This is because the platform executes some operations between the record change and is cancelled before audit creation. But, now audits are created immediately after the record is changed, reducing the chances of a cancelled transaction aborting the operation before the audit is recorded.

Audits are now recorded in the same thread as the transaction. Earlier audits were created in a background thread. This change redefines the default value of the `glide.db.audit.lazy` property from True to False. This property is not usually defined in the Properties table because the majority of instances start using the new default value and behavior. On some instances, this property might be already present and set as True, which means that these instances won’t be able to use this change to audit behavior.

**Note:** It is recommended to delete this property to leverage the update.

