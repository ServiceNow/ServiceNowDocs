---
title: Upgrade Monitor overview
description: The Upgrade Monitor helps you upgrade an individual instance. You can monitor the progress of an upgrade and resolve conflicts between the upgrade and customizations.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Upgrade Monitor module: Upgrade an individual instance, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Monitor overview

The Upgrade Monitor helps you upgrade an individual instance. You can monitor the progress of an upgrade and resolve conflicts between the upgrade and customizations.

## Set up for the Upgrade Monitor

In Xanadu, the Upgrade Monitor is installed by default.

If you log in with the admin role while an upgrade is underway, the system automatically displays the Upgrade Progress screen. If no upgrade is in progress, you can navigate to **System Diagnostics** &gt; **Upgrade Monitor**.

## How the Upgrade Monitor fits into the upgrade process

**Note:** For detailed information about the upgrade process, see [Upgrade your instance](https://www.servicenow.com/docs/access?context=upgrades-overview&version=xanadu&pubname=xanadu-release-notes&ft:locale=en-US).

The Upgrade Monitor concerns only part of the larger upgrade process:

1.  Clone the production instance to a test instance and a non-production instance.
2.  Apply the upgrade to the non-production instance.
3.  On the upgraded non-production instance, [Process the skipped records list](../task/upgrademon-process-skip-list.md)
4.  Test the non-production instance to confirm that the instance still works and performs adequately. Compare to benchmark data from pre-upgrade production instance.
5.  Apply the upgrade to the test instance. Import the update sets created on the non-production instance when you processed the skipped list. Repeat the testing to make sure that the process is working.
6.  Apply the upgrade to the production instance. Import the update sets created on the non-production instance when you processed the skipped list. Test to confirm that the instance works and performs adequately.

Within this larger process, the Upgrade Monitor helps you upgrade individual instances:

-   during the upgrade, it shows where in the process the system is
-   after the upgrade, it reports what the upgrade did and for how long
-   as you upgrade the first non-production instance, it helps you resolve conflicts between customizations and changes that are part of the upgrade
-   on non-production instances, it provides information that can help you estimate how long the upgrade takes on the production instance.

**Note:** Debug Upgrade provides detailed debugging output for transactions containing artifacts affected by the most recent upgrade, and is designed to assist in upgrade error resolution. See [Debug upgrade](../reference/debug-upgrade.md).

## Monitoring an individual instance as it upgrades

While the upgrade is in progress the [Upgrade Progress](../reference/upgrademon-upgrade-progress-scrn.md) shows what the upgrade process has done, what it is doing, and what remains to be done.

When the upgrade completes, the system displays the [Upgrade Summary Report](../reference/upgrademon-upgrade-summary-rpt.md). The Upgrade Summary Report provides information about conflicts between customizations versus the upgrade and provides a link to reconcile these conflicts. For information about understanding and resolving these conflicts, see [Resolve Conflicts form](../reference/upgrademon-resolve-conflicts-form.md).

When you upgrade a non-production instance, the Upgrade Summary Report can help you estimate how long the same upgrade takes on a production instance. For details about the elements on this report and how to use this information, see [Upgrade Progress](../reference/upgrademon-upgrade-progress-scrn.md).

## Resolving conflicts

To prevent losing customizations, the system skips upgrading records you have customized and provides you with a list of these skipped records.

As you upgrade your first non-production instance, go through the [Skipped Changes to Review related list](../../../customer-support/concept/skipped-changes-to-review-related-list.md) and resolve these conflicts. The system records the changes you make during this process in update sets.

You do not need to reconcile the skipped list on any instances you later upgrade. Instead, you can apply the upgrade then import the update sets containing your changes.

For details on reconciling conflicts, see [Process the skipped records list](../task/upgrademon-process-skip-list.md).

