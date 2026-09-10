---
title: Exploring Instance Clone
description: Explore how to use a clone to copy everything in a database from one instance to another.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/exploring-instance-clone.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Exploring Instance Clone

Explore how to use a clone to copy everything in a database from one instance to another.

## Instance Clone overview

Clone copies data and configuration from a source instance to a target instance, overwriting the target. After a clone, your environment closely resembles the source instance and allows you to safely test changes. Sub-production instances drift from production over time; clone resets that divergence.

Common use cases include:

-   Validating upgrades
-   Testing new applications
-   Testing new capabilities

Clone data is sourced from the most recent daily backup of the source instance.

For clone terminology and definitions, see [Clone terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-terminology.md).

## Instance Clone workflow

\[Omitted image "instance-clone-workflow-diagram-final.png"\] Alt text: Instance clone workflow diagram.

1.  Clone build configuration: Basic definitions, configurations, and profile options are prepared. Data to be included, excluded, or preserved is verified.

2.  Preflight checks: The clone checks the source and target instances to verify that they are in a healthy state before proceeding with the clone.
3.  Backup: Uses the latest daily backup. If there were major recent changes, a new backup is created. You can also trigger a new backup manually by selecting **On-demand backup** in the **Clone Admin Console**.

4.  Pre-Clone: Prepares space for the new database before restoring it.

5.  Provision database instance \(DBI\): A new target instance is set up to receive the restored data.

6.  Restore: The backup data is restored to the new target instance.

7.  Exclusions: Tables marked for exclusion are deleted.

8.  Preservers: Data is preserved from the old target \(pre-clone instance\) and is copied to the new target instance.

9.  Node repoint: The system switches from the old target to the new clone without user disruption.
10. Scheduling scripts: All scripts are scheduled to run in the global scope. Starting with the Australia Patch 5 release, script status is visible. Any changes to cleanup scripts, which are defined on the source, must happen before the Restore phase of a clone to be processed within that clone request.
11. Post Clone: The instance is set up in its own phase. Cleanup scripts run after the clone shows as Complete. To view cleanup script status on the source instance, enable **Multi-Instance View**. Both instances must be on Australia Patch 5 or later.


## Instance Clone users

|User|Description|
|----|-----------|
|Clone Administrator|Clone admins with the **clone\_admin** role can request, cancel, or schedule clones.|

## Instance Clone benefits

|Benefit|Feature|
|-------|-------|
|Tidy up data with exclusions and preservers for specific clone scenarios.|[Definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-exclusions-preservers-cleanupscripts.md)|
|Establish consistent clone outcomes with clone profiles and registered instances.|[Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-configurations-tab.md)|
|Copy data from a production instance to a non-production instance or to copy data between non-production instances.|[Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md)|

## Instance Clone use cases

## Clone to a different version

You can clone between instances that are on different family release versions. During a clone, the source version replaces the target version. For example, if you clone from Source \(Zurich\) to Target \(Yokohama\) the target will match the source after the clone and be on Zurich release.

## Clone from a backup

The clone uses data from the most recent, daily backup of the source instance when cloning. Backups that are used for cloning are a maximum of 36 hours old. A clone from backup starts only at the date and time processing that it's scheduled to start.

If the source and target instances are on different versions of the ServiceNow AI Platform, the target instance is modified to match the source instance version during this time.

When starting a clone from a backup, the Clone log displays the date and time the backup was taken. Periodic progress messages also appear in the Clone log at the bottom of the clone status page.

## Clone over production instances

As long as the system property **glide.db.clone.allow\_clone\_target** is `TRUE`, an instance can serve as a clone target. Ensure the property **glide.db.clone.allow\_clone\_target** is set back to `FALSE` after a production instance has served as a clone target. This prevents accidental clones over production in the future.

**Note:** Beginning with the Australia release, users attempting to access the legacy Instance Clone page, **clone\_instance.do**, are redirected instead to the [Clone Admin Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/Clone-UI.md). To view clone history for clones prior to the Australia release, view the legacy Clone History \[clone\_instance\] table.

For more information about using Clone Admin Console instead of the legacy Instance Clone, see [KB1425858: Clone Admin Console: Quick Start Guide &amp; Instructions](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1425858).

