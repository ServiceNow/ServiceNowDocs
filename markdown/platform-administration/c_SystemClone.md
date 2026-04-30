---
title: System clone
description: Use the System Clone application to copy everything in a database from one instance to another.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure core features, Administer the ServiceNow AI Platform]
---

# System clone

Use the System Clone application to copy everything in a database from one instance to another.

Cloning is typically used to copy a production instance to a pre-production instance to test changes. Cloning data comes from the most recent nightly backup.

**Note:** A new, unified admin experience based on the existing clone engine is now available in the [Clone Admin Console](Clone-UI.md). The Clone Admin Console provides enhanced visibility for cloning data between instances, one of our most-used automations, as well as a number of other enhancements.

![Clone process overview](../image/CloneProcess.png "Clone process")

In response to a clone request, the ServiceNow platform performs the following tasks:

1.  Generates a file to preserve operational data on the target server.

    **Note:** This file contains the data preserved by [data preservers](data-preservation.md#).

2.  Copies the database schema from the source instance to the target instance.
3.  Creates tables in the target instance database using the source instance table definitions.
4.  Copies data from the most recent nightly backup of the source instance to the target instance database.

    **Note:** Certain exclusions are automatic, large tables are normally excluded. These include audit, log, and email tables. MetricBase tables aren’t excluded by default.

5.  Briefly disables UI traffic and requests to the target instance server.
6.  Displays the message **Clone in progress...** to any user accessing the target instance.
7.  Restores operational data preserved from the target instance.
8.  Runs any post-clone cleanup scripts on the target instance.
9.  Briefly suspends all email functions on the target instance.
10. Queues an event to regenerate text indexes.
11. Enables UI traffic and requests to the target instance server.

During a clone, the target instance may be intermittently unavailable. After clone completion, you have up to 24 hours to contact Customer Service and Support and request a rollback of the target instance to its pre-clone state. You’re notified when the rollback is complete.

**Note:** If the source instance has a clone depth level of &gt;=5 then the clone isn’t allowed.

If the source instance purpose is DART \(Data Access for Responsible Training\) then the clone isn’t allowed and an error message will be displayed.

## Clone to an instance on a different version

The System Clone application can target an instance running a different instance version from the source.

A central web service controls the clone processing and automatically modifies the target instance version to match the source instance version. This matching process starts up to eight hours before the time specified in the **Date and time** field on the System Clone form. This web service also confirms that there’s enough disk space on the target instance for the clone to proceed.

When cloning from a backup, the target instance doesn’t need additional time to upgrade or downgrade. The ServiceNow platform performs any version changes during a brief window where the target instance is unavailable, after it copies data from the source instance backup.

## Clone from a backup

The clone uses data from the most recent, nightly backup of the source instance when cloning. Backups that are used for cloning are a maximum of 36 hours old. System Clone begins the initial preparation, including selecting the latest backup to use, only at the date and time processing is scheduled to start.

If cloning from a source backup fails, the system uses the legacy clone engine instead. The legacy clone engine can’t preserve data from extended tables, relationships, hierarchies between tables, and dot-walked queries. You may want to restore the target instance from a backup and then reschedule the clone in such cases.

After cloning from a backup, the target instance is unavailable for several minutes before the clone is marked as complete in the source instance. If the source and target instances are on different versions of the ServiceNow AI Platform, the target instance is modified to match the source instance version during this time.

When starting a clone from a backup, the date and time the backup was taken, as well as periodic progress messages, appear in the **Clone Log** related list.

![Clone log backup record](../image/SystemCloneBackupLog2.png "System clone backup log")

## Clone over production instances

As long as the system property **glide.db.clone.allow\_clone\_target** is TRUE, an instance can serve as a clone. Modifying data on the source instance during a clone can cause a data mismatch between records or duplicate record entries.

## Deprecated Clone Options

The clone option check box **Preserve users and related tables** has been removed from Clone Options in the Utah release. In some cases, past customizations to the clone request page or related to clone, may cause this field to remain on your form.

**Important:** Checking this deprecated field won’t have any effect on the user, role, or related tables during your clone.

.

