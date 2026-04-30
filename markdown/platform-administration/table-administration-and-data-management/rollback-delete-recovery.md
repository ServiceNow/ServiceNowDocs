---
title: Roll back and delete recovery
description: With rollback contexts, you can roll back certain actions such as a patch upgrade, plugin activation, and background script executions, and you can recover record deletions and all related changes.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Roll back and delete recovery

With rollback contexts, you can roll back certain actions such as a patch upgrade, plugin activation, and background script executions, and you can recover record deletions and all related changes.

The roll back and delete recovery features are available on instances that use MySQL and MariaDB databases. Instances that use Oracle databases only support roll back. Instances that use SQL Server do not support roll back or delete recovery.

|Database type|Roll back|Delete recovery|
|-------------|---------|---------------|
|MySQL|yes|yes|
|MariaDB|yes|yes|
|Oracle|yes|no|

## Deleted Records module

This module works on records in audited tables. Recovery of cascaded deleted records must be done within seven days of the record deletion. After seven days, only data records and references on tables that audit deletions can be recovered, which is the same functionality as prior releases.

To find this module, navigate to **System Definition** &gt; **Deleted Records**.

## Delete Recovery module

This module works for any deleted record. This recovery must be done within seven days of the record deletion.

To find this module, navigate to **Rollback &amp; Recovery** &gt; **Delete Recovery**.

## Script Execution History module

This module works on scripts executed using the **Scripts - Background** module. This history only includes seven days of script executions.

To find this module, navigate to **Rollback &amp; Recovery** &gt; **Script Execution History**.

## Rollback contexts

Rollback contexts contain everything necessary to roll back a software upgrade or plugin activation. They include deleted records, patch updates, Scripts-Background script executions, database actions, and plugin activations. A rollback context is created for each patch upgrade within a family, and each plugin activation, provided that the plugin supports rollback contexts.

To use rollback contexts, activate the Restore Deleted Records \(com.snc.undelete\) and Delete Recovery \(com.glide.delete\_recovery\) plugins.

Rollbacks are typically performed on pre-production instances where functionality must be restored before you can find the root cause of a problem in the upgrade. Rolling back deletes data, which can often make it hard if not impossible to discover the problem that made the rollback necessary.

A rollback context is created when:

-   GlideRecord.delete\(\) or GlideRecord.deleteMultiple\(\) delete records.
-   There is a patch upgrade.
-   You activate a plugin that supports rollback contexts.
-   A script executes using the **Scripts-Background** module, and rollback was enabled by selecting the **Record for Rollback?** check box.

Rollbacks do not impact other database activities. If a database activity modifies a record that is part of a rollback context, the rollback does not affect that record.

Because rollback contexts contain a significant amount of data, rollback contexts are deleted after 10 days. Therefore, rollbacks must occur within 10 days of the latest upgrade or plugin activation. If you need to retain a rollback context for more than 10 days, you can do so by adding a system property. See [Rollback context properties](../reference/rollback-context-properties.md).

**Note:** Do not roll back a rollback context until checking with Customer Service and Support. A roll back deletes data and may remove evidence of the upgrade or activation issue preventing debugging of the problem.

To find this module, navigate to **Rollback &amp; Recovery** &gt; **Rollback Contexts**.

If any of the following operations occur during a rollback, a rollback context is not created:

-   Tables or columns are dropped from the schema.

    **Note:** Index drops are okay.

-   A table is truncated.
-   A table or column is renamed.
-   A column is re-parented or promoted.
-   A column type changes.
-   A column width is decreased.

The rollback process on Now Support does the following:

-   Updates the reported WAR to the rolled-back version and the assigned WAR remains set to the version before the rollback.
-   Sets the property **glide.war.no\_upgrade** on the instance is set to the version before the rollback.
-   Displays the message, "Desired war matches reverted war specified by property \[**glide.war.no\_upgrade**\]. Upgrade script will NOT run".
-   Changes the state to **Expired** and the rollback purges all stored data.

-   **[Roll back patch upgrades or plugin activations](../task/roll-back-rollback-context.md)**  
Use the **Rollback Contexts** module to roll back patch upgrades and plugin activations.
-   **[Use the Deleted Records module to restore a deleted record](../task/t_RestoreADeletedRecordAndRef.md)**  
You can recover deleted records that are in audited tables.
-   **[Use the Delete Recovery module to restore a deleted record](../task/delete-recovery.md)**  
You can recover a deleted record and all related changes. The recovery must be done within seven days of the record being deleted.
-   **[Use the Script Execution History module to roll back a Scripts-Background execution](../task/background-script-recovery.md)**  
You can roll back the database actions of a script executed using the Scripts-Background module.
-   **[Rollback context properties](../reference/rollback-context-properties.md)**  
Change the default expiration period for different types of rollback context records.

**Parent Topic:**[ServiceNow AI Platform tables and data](../../general/concept/tables-fields-and-forms.md)

