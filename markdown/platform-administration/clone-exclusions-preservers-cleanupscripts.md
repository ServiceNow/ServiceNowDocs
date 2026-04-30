---
title: Definitions
description: Use clone definitions such as exclusions, preservers, and cleanup scripts in your clone.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-09-24"
reading_time_minutes: 4
breadcrumb: [Explore, Instance Clone, Configure core features, Administer]
---

# Definitions

Use clone definitions such as exclusions, preservers, and cleanup scripts in your clone.

The **Definitions** page displays an overview for exclusions, preservers, and cleanup scripts.

## Exclusions

The exclusions page lists the tables that aren’t copied during an instance clone. When excluding a table, the clone automation truncates the entire table including its child tables. The clone process excludes \(or removes\) data from both the parent and the child tables. The child tables, however, aren't individually added to the list of excluded tables. Only the parent table is listed.

To view child tables of a table, you can go to the following link and input their table: **\[instance\].service-now.com/now/nav/ui/classic/params/target/generic\_hierarchy\_erd.do**.

By default, the system excludes tables for logging, auditing, notifications, workflow contexts, and license usage. To configure additional exclusions, see [Exclude a table from cloning \(legacy\)](../task/t_ExcludeATableFromCloning.md).

For information on guidelines when adding exclusions see [General guidelines for excluding a table from cloning](../reference/clone-exclusions-guidelines.md).

## Preservers

The preservers page displays a list of available data preservers, which are defined on the source instance. Preservers protect data on the target instance from being overwritten.

Preservers work differently compared to exclusions. When preserving a table, the clone automation doesn’t automatically preserve the child tables. Therefore, the child tables must be individually added to the preserver list. To create a preserver see [Create a clone preserver](../task/create-new-clone-preserver.md).

## Cleanup scripts

The cleanup scripts page displays a list of all of your available scripts. Cleanup scripts automate post-clone steps.

Set an order number on each script, to set the order that the active scripts run, with lower numbers having a higher priority. To run some scripts in parallel, you can assign the same order to them.

All cleanup scripts run in the global scope irrespective of the scope in which you have configured the cleanup script.

|Script|Description|
|------|-----------|
|Bad MID Server credentials after clone|Runs a script include called BadMIDCredentialAfterClone on a cloned instance to detect [bad MID Server user credentials](https://www.servicenow.com/docs/access?context=mid-post-clone-issue-resolution&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). This script include creates scheduled jobs that log MID Servers in the **Down** state to the MID Server Issue \[ecc\_agent\_issue\] table after an instance clone.|
|Clear scheduled job node association|Resets any scheduled jobs that were active on the source instance to the **Ready** state. This script also clears the value of the **System ID** and **Claimed by** fields on all scheduled jobs.|
|Configure Email Accounts|Migrates email accounts that existed on the source instance to the target instance if they aren’t enabled there. This script also migrates the email properties to the target instance.|
|Disable emails|Disables email on the target instance. A default data preserver maintains other email settings from the target instance.|
|Install deactivated plugin|Enables the Domain Separation plugin for instances that use this feature.|
|Regenerate all text indexes|Rebuilds text indexes on the target instance after a clone. Text indexes aren’t cloned from the source to the target instance.|
|Schedule drop backup tables|Schedules the deletion of the data that is contained in the target instance database before the clone. This original data is preserved for 24 hours following a clone to enable you to roll back an instance to the pre-clone state. If the target instance is downgraded as part of the clone, backup data isn’t available.|

**Note:** After the clone completes, all active cleanup scripts are combined together as a scheduled job named **Execute Clone Cleanup Script: Execute Cleanup Scripts Sequentially** and run until completion in the global scope.

To create a cleanup script see [Create cleanup scripts](../task/create-cleanup-script.md).

## Clarifying exclusions and preservers combinations

Clone exclusions and preservers are both useful for managing your data. The graphics help to identify the expected outcome of the following combinations of preservers and exclusion combinations. For more information, see the [February 2025 Platform Fundamentals Academy session on Clone Admin Console](https://www.servicenow.com/community/servicenow-ai-platform-blog/platform-fundamentals-academy-february-20th-2025-clone-admin/ba-p/3170929).

![Clone exclusions and preservers cheatsheet.](../image/clone-exclusion-preservers-cheatsheet.png)

-   Scenario 1: Preserving and excluding a table. You want the records on your target instance to remain the same.
-   Scenario 2: Preserving and not excluding a table. You want records on your target Instance to remain the same and records for your source instance to be copied over.
-   Scenario 3: Not preserving and excluding a table. You want records from your source instance not to be copied over and records on your target instance to be removed: The table is empty but usable after the clone.
-   Scenario 4: Not preserving and not excluding a table. You want records from your source instance to replace records on your target instance.

**Important:** During a clone, data from the source instances replaces data from the target instance. Therefore, any in-progress development work on the target instance is overwritten. For example: Work-in-progress update sets, scoped apps that only exist on the target instance but not on the source instance. If you have in-progress update sets, you must export them before the clone and re-import them after the clone is finished. Custom applications that aren't yet deployed to the source instance must be reinstalled after the clone is completed.

To learn more about clone and app development tips, see the [Leveraging System Clones for Seamless Development and Deployment Whitepaper](https://learning.servicenow.com/nowcreate/en?id=nc_asset&asset_id=ce3c254697cc82d06eedb30e6253af3b&nc_source=copy_asset_link).

