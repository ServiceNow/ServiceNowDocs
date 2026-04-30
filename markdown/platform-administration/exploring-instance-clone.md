---
title: Exploring Instance Clone
description: Explore how to use a clone to copy everything in a database from one instance to another.The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.Use clone definitions such as exclusions, preservers, and cleanup scripts in your clone.Use the configurations page to add clone instances or create clone profiles.Cloning is the easiest way to synchronize your instances. You can clone to a different version, clone from a backup, or clone over production instances.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-09-24"
reading_time_minutes: 11
breadcrumb: [Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Exploring Instance Clone

Explore how to use a clone to copy everything in a database from one instance to another.

## Clone overview

Cloning is the easiest way to synchronize your instances. It’s essential to have a representative environment to test changes before they go to production.

-   Cloning helps reduce divergence between the environments and promotes smooth deployments.
-   Cloning is used to test changes such as upgrades, new applications, and new capabilities.
-   Cloning data comes from the most recent daily backup.

A list of helpful terminology and definitions for clone is included here [Clone terminology](../reference/clone-terminology.md).

## Instance Clone workflow

![Instance clone workflow diagram.](../image/instance-clone-workflow-diagram-final.png "Instance Clone workflow diagram")

1.  Clone build configuration: Basic definitions, configurations, and profile options are prepared. Data to be included, excluded, or preserved is verified.

2.  Preflight checks: The clone checks the source and target instances to verify that they are in a healthy state before proceeding with the clone.
3.  Backup: Uses the latest daily backup. If there were major recent changes, a new backup is created. You can also trigger a new backup manually by selecting the On-demand backup via the Clone Admin Console.

4.  Pre-Clone: Prepares space for the new database before restoring it.

5.  Provision database interface \(DBI\): A new target instance is set up to receive the restored data.

6.  Restore: The backup data is restored to the new target instance.

7.  Exclusions: Tables marked for exclusion are deleted.

8.  Preservers: Data is preserved from the old target \(pre-clone instance\) and is copied to the new target instance.

9.  Node repoint: The system switches from the old target to the new clone without user disruption.
10. Scheduling scripts: Cleanup scripts and custom scripts are scheduled to run. Scripts with the same priority run at the same time.
11. Post Clone: Cleanup scripts run.


## Clone users

|User|Description|
|----|-----------|
|Administrator|Clone admins with the `clone_admin` role can request, cancel, schedule, or modify clones.|

## Clone benefits

|Benefit|Feature|
|-------|-------|
|Tidy up data with exclusions and preservers for specific clone scenarios.|[Definitions](exploring-instance-clone.md#)|
|Establish consistent clone outcomes with clone profiles and registered instances.|[Configurations](exploring-instance-clone.md#)|
|Copy data from a production instance to a non-production instance or to copy data between non-production instances.|[Request a clone](../task/t_StartAClone.md#)|

## Clone Admin Console

The Clone Admin Console is the user interface where administrators can manage, request, and monitor their instance clones.

### Clone Home

The home page displays the current clones in your instance. Use the search bar to locate your clone.

Filter options enable you to locate a clone based on its status. To view a list of statuses, see [Clone states](../reference/clone-states.md).

**Note:** The clone home page displays clones requested through the Clone Admin Console. You can't view clones requested through the legacy request page `(clone_instance.do)` in the dashboard. To view legacy clones in either a grid or list view, navigate to **All** &gt; **Instance Clone** &gt; **Live Clones** &gt; **Clone History**.

![clone home dashboard.](../image/cac-dashboard.png)

### Configurations

The configurations tab displays an overview and information about clone instances and clone profiles. See [Configurations](exploring-instance-clone.md#) for more information.

### Definitions

The definitions tab displays an overview for exclusions, preservers, and cleanup scripts. See [Definitions](exploring-instance-clone.md#) for more information.

### Request clone

The clone request page contains guidance and explanations for how the various clone settings affect your clone. You can use the scheduling calendar to help to prevent timing conflicts with ServiceNow maintenance windows. To learn more about how to request a clone see [Request a clone](../task/t_StartAClone.md#).

### Deprecated Clone Options

The clone option check box **Preserve users and related tables** was removed from the [Clone options](../reference/clone-options.md) in the Utah release. In some cases, past customizations to the clone request page or related to clone, may cause this field to remain on your form.

**Important:** Selecting this deprecated field doesn't effect the user, role, or related tables during your clone.

.

You can't request new clones through the legacy request page **clone\_instance.do**. For more information see [Request a clone \(legacy\)](../task/t_StartAClone.md#).

## Definitions

Use clone definitions such as exclusions, preservers, and cleanup scripts in your clone.

The **Definitions** page displays an overview for exclusions, preservers, and cleanup scripts.

### Exclusions

The exclusions page lists the tables that aren’t copied during an instance clone. When excluding a table, the clone automation truncates the entire table including its child tables. The clone process excludes \(or removes\) data from both the parent and the child tables. The child tables, however, aren't individually added to the list of excluded tables. Only the parent table is listed.

To view child tables of a table, you can go to the following link and input their table: **\[instance\].service-now.com/now/nav/ui/classic/params/target/generic\_hierarchy\_erd.do**.

By default, the system excludes tables for logging, auditing, notifications, workflow contexts, and license usage. To configure additional exclusions, see [Exclude a table from cloning \(legacy\)](../task/t_ExcludeATableFromCloning.md).

For information on guidelines when adding exclusions see [General guidelines for excluding a table from cloning](../reference/clone-exclusions-guidelines.md).

### Preservers

The preservers page displays a list of available data preservers, which are defined on the source instance. Preservers protect data on the target instance from being overwritten.

Preservers work differently compared to exclusions. When preserving a table, the clone automation doesn’t automatically preserve the child tables. Therefore, the child tables must be individually added to the preserver list. To create a preserver see [Create a clone preserver](../task/create-new-clone-preserver.md).

### Cleanup scripts

The cleanup scripts page displays a list of all of your available scripts. Cleanup scripts automate post-clone steps.

Set an order number on each script, to set the order that the active scripts run, with lower numbers having a higher priority. To run some scripts in parallel, you can assign the same order to them.

All cleanup scripts run in the global scope irrespective of the scope in which you have configured the cleanup script.

|Script|Description|
|------|-----------|
|Bad MID Server credentials after clone|Runs a script include called BadMIDCredentialAfterClone on a cloned instance to detect [bad MID Server user credentials](https://www.servicenow.com/docs/access?context=mid-post-clone-issue-resolution&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). This script include creates scheduled jobs that log MID Servers in the **Down** state to the MID Server Issue \[ecc\_agent\_issue\] table after an instance clone.|
|Clear scheduled job node association|Resets any scheduled jobs that were active on the source instance to the **Ready** state. This script also clears the value of the **System ID** and **Claimed by** fields on all scheduled jobs.|
|Configure Email Accounts|Migrates email accounts that existed on the source instance to the target instance if they aren’t enabled there. This script also migrates the email properties to the target instance.|
|Disable emails|Disables email on the target instance. A default data preserver maintains other email settings from the target instance.|
|Install deactivated plugin|Enables the Domain Separation plugin for instances that use this feature.|
|Regenerate all text indexes|Rebuilds text indexes on the target instance after a clone. Text indexes aren’t cloned from the source to the target instance.|
|Schedule drop backup tables|Schedules the deletion of the data that is contained in the target instance database before the clone. This original data is preserved for 24 hours following a clone to enable you to roll back an instance to the pre-clone state. If the target instance is downgraded as part of the clone, backup data isn’t available.|

**Note:** After the clone completes, all active cleanup scripts are combined together as a scheduled job named **Execute Clone Cleanup Script: Execute Cleanup Scripts Sequentially** and run until completion in the global scope.

To create a cleanup script see [Create cleanup scripts](../task/create-cleanup-script.md#).

### Clarifying exclusions and preservers combinations

Clone exclusions and preservers are both useful for managing your data. The graphics help to identify the expected outcome of the following combinations of preservers and exclusion combinations. For more information, see [https://www.servicenow.com/community/servicenow-ai-platform-blog/platform-fundamentals-academy-february-20th-2025-clone-admin/ba-p/3170929](https://www.servicenow.com/community/servicenow-ai-platform-blog/platform-fundamentals-academy-february-20th-2025-clone-admin/ba-p/3170929)

![Clone exclusions and preservers cheatsheet.](../image/clone-exclusion-preservers-cheatsheet.png)

-   Scenario 1: Preserving and excluding a table. You want the records on your target instance to remain the same.
-   Scenario 2: Preserving and not excluding a table. You want records on your target Instance to remain the same and records for your source instance to be copied over.
-   Scenario 3: Not preserving and excluding a table. You want records from your source instance not to be copied over and records on your target instance to be removed: The table is empty but usable after the clone.
-   Scenario 4: Not preserving and not excluding a table. You want records from your source instance to replace records on your target instance.

During a clone, data from the source instances replaces data from the target instance. Therefore, any in-progress development work on the target instance is overwritten. For example: Work-in-progress update sets, scoped apps that only exist on the target instance but not on the source instance. If you have in-progress update sets, you must export them before the clone and reimport them after the clone is finished. Custom applications that aren't yet deployed to the source instance must be reinstalled after the clone is completed.

To learn more about clone and app development tips, see Whitepaper [here](https://learning.servicenow.com/nowcreate/en?id=nc_asset&asset_id=ce3c254697cc82d06eedb30e6253af3b&nc_source=copy_asset_link).

## Configurations

Use the configurations page to add clone instances or create clone profiles.

**Before you begin**

-   You can add external email addresses to receive clone notifications.
-   Some default items can't be removed from the exclusions, preservers, or scripts list.

### Configurations overview

The overview page displays the current number of clone instances and clone profiles in your instance.

### Clone instances

The clone instances page displays all available instances. You can use instances added to this list as a clone source or clone target for your clones. To add your non-production instance to your clone instances list, select **New**.

### Clone profiles

Clone profiles display all available profiles. Clone profiles are customizable templates for clones and can be saved and reused to achieve consistent outcomes with each of your clones. To learn more about Clone Profiles, see [Create a custom clone profile](../task/configure-clone-profile.md).

The profile System Profile is available by default and can't be modified. Custom profiles use the default Exclusions, Preservers, and Scripts from the System Profile. When creating a custom profile, all existing custom exclusions and preservers are automatically added.

You can create as many custom clone profiles as you'd like and edit them as needed. To change the definitions of a clone profile, such as exclusions, preservers or cleanup scripts, select the number under the definition and select the **Edit** button on the page.

## Clone use cases

Cloning is the easiest way to synchronize your instances. You can clone to a different version, clone from a backup, or clone over production instances.

### Clone to an instance on a different version

### Clone to a different version

You can clone between instances that are on different family release versions. During a clone, the source version replaces the target version. For example, if you clone from Source \(Zurich\) to Target \(Yokohama\) the target will match the source after the clone and be on Zurich release.

.

### Clone from a backup

The clone uses data from the most recent, daily backup of the source instance when cloning. Backups that are used for cloning are a maximum of 36 hours old. A clone from backup starts only at the date and time processing that it's scheduled to start.

If the source and target instances are on different versions of the ServiceNow AI Platform, the target instance is modified to match the source instance version during this time.

When starting a clone from a backup, the date and time the backup was taken, as well as periodic progress messages, appear in the **Clone Log** related list.

### Clone over production instances

As long as the system property **glide.db.clone.allow\_clone\_target** is TRUE, an instance can serve as a clone.

### Deprecated Clone Options

The clone option check box **Preserve users and related tables** was removed from the Clone Options in the Utah release. In some cases, past customizations to the clone request page or related to clone, may cause this field to remain on your form.

**Important:** Selecting this deprecated field doesn't effect the user, role, or related tables during your clone.

.

You can't request new clones through the legacy request page **clone\_instance.do**. For more information, see [Request a clone \(legacy\)](../task/t_StartAClone.md#).

