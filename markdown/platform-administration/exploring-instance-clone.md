---
title: Exploring Instance Clone
description: Explore how to use a clone to copy everything in a database from one instance to another.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-02"
reading_time_minutes: 3
breadcrumb: [Instance Clone, Configure core features, Administer]
---

# Exploring Instance Clone

Explore how to use a clone to copy everything in a database from one instance to another.

## Instance Clone overview

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


## Instance Clone users

|User|Description|
|----|-----------|
|Administrator|Clone admins with the `clone_admin` role can request, cancel, schedule, or modify clones.|

## Clone benefits

|Benefit|Feature|
|-------|-------|
|Tidy up data with exclusions and preservers for specific clone scenarios.|[Definitions](clone-exclusions-preservers-cleanupscripts.md)|
|Establish consistent clone outcomes with clone profiles and registered instances.|[Configurations](clone-configurations-tab.md)|
|Copy data from a production instance to a non-production instance or to copy data between non-production instances.|[Request a clone](../task/t_StartAClone.md)|

## Instance Clone use cases

## Clone to a different version

You can clone between instances that are on different family release versions. During a clone, the source version replaces the target version. For example, if you clone from Source \(Zurich\) to Target \(Yokohama\) the target will match the source after the clone and be on Zurich release.

## Clone from a backup

The clone uses data from the most recent, daily backup of the source instance when cloning. Backups that are used for cloning are a maximum of 36 hours old. A clone from backup starts only at the date and time processing that it's scheduled to start.

If the source and target instances are on different versions of the ServiceNow AI Platform, the target instance is modified to match the source instance version during this time.

When starting a clone from a backup, the date and time the backup was taken, as well as periodic progress messages, appear in the **Clone Log** related list.

## Clone over production instances

As long as the system property **glide.db.clone.allow\_clone\_target** is TRUE, an instance can serve as a clone target. Please ensure the property **glide.db.clone.allow\_clone\_target** is set back to FALSE after a production instance has served as a clone target. This helps prevent accidental or unintended clones over production in the future.

## Deprecated Clone Options

The clone option check box **Preserve users and related tables** was removed from the Clone Options in the Utah release. In some cases, past customizations to the clone request page or related to clone, may cause this field to remain on your form.

**Important:** Selecting this deprecated field doesn't effect the user, role, or related tables during your clone.

**Note:** Beginning with the Australia release, users attempting to access the legacy Instance Clone page, **clone\_instance.do**, are redirected instead to the [Clone Admin Console](Clone-UI.md). To view clone history for clones prior to the Australia release, view the legacy Clone History \[clone\_instance\] table.

For more information about using Clone Admin Console instead of the legacy Instance Clone, see [KB1425858: Clone Admin Console: Quick Start Guide &amp; Instructions](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1425858).

