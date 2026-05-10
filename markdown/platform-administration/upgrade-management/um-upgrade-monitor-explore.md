---
title: Explore Upgrade Monitor in Upgrade Console
description: The Upgrade Monitor module is a powerful tool for scheduling upgrades, monitoring their progress, and analyzing post-upgrade results, including conflict resolution.
locale: en-US
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Upgrade Console summary, Explore, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Explore Upgrade Monitor in Upgrade Console

The Upgrade Monitor module is a powerful tool for scheduling upgrades, monitoring their progress, and analyzing post-upgrade results, including conflict resolution.

## Access Upgrade Monitor

If you log in with the admin role while an upgrade is underway, the system automatically displays the Upgrade Progress screen. If no upgrade is in progress, you can follow one of the following ways.

|Option|Navigation|
|------|----------|
|Using left navigation|Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Console** &gt; **Upgrade Monitor**.|
|Using Admin tab option|Navigate to **Admin** &gt; **Upgrade Console** &gt; **Upgrade Monitor**.|

## How the Upgrade Monitor fits into the upgrade process

**Note:** For detailed information about the upgrade process, see [Upgrade your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/upgrades-overview.md).

The Upgrade Monitor concerns only part of the larger upgrade process:

1.  Clone the production instance to a test instance and a non-production instance.
2.  Apply the upgrade to the non-production instance.
3.  On the upgraded non-production instance, [Process the skipped records list](../task/um-process-skipped-records.md).
4.  Test the non-production instance to confirm that the instance still works and performs adequately. Compare to benchmark data from pre-upgrade production instance.
5.  Apply the upgrade to the test instance. Import the update sets created on the non-production instance when you processed the skipped list. Repeat the testing to make sure that the process is working.
6.  Apply the upgrade to the production instance. Import the update sets created on the non-production instance when you processed the skipped list. Test to confirm that the instance works and performs adequately.

Within this larger process, the Upgrade Monitor helps you upgrade individual instances:

-   During the upgrade, it shows where in the process the system is
-   After the upgrade, it reports what the upgrade did and for how long
-   As you upgrade the first non-production instance, it helps you resolve conflicts between customizations and changes that are part of the upgrade
-   On non-production instances, it provides information that can help you estimate how long the upgrade might take on the production instance

## Monitoring an individual instance as it upgrades

While the upgrade is in progress the Upgrade Progress shows what the upgrade process has done, what it is doing, and what remains to be done.

When the upgrade completes, the system displays the Upgrade Summary Report. The Upgrade Summary Report provides information about conflicts between customizations versus changes in the upgrade and provides a link to reconcile these conflicts. For information about understanding and resolving these conflicts, see [Process the skipped records list](../task/um-process-skipped-records.md) list.

When you upgrade a non-production instance, the Upgrade Summary Report can help you estimate how long the same upgrade might take on a production instance. For details about the elements on this report and how to use this information, see [Upgrade details form](../reference/um-upgrade-details-form.md).

## Resolving conflicts

To prevent losing customizations, the system skips upgrading records you have customized and provides you with a list of these skipped records.

As you upgrade your first non-production instance, go through the Skipped Changes to Review related list and resolve these conflicts. The system records the changes you make during this process in update sets. See [Review skipped records using related lists](../task/um-access-rl.md#), for more information.

You do not need to reconcile the skipped list on any instances you later upgrade. Instead, you can apply the upgrade then import the update sets containing your changes.

For details on reconciling conflicts, see [Process the skipped records list](../task/um-process-skipped-records.md).

See [Upgrade Monitor tool in Upgrade Console](um-upgrade-monitor-tool.md) for more information.

