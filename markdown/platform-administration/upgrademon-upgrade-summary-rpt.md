---
title: Upgrade Summary Report
description: This report summarizes the actions taken, provides tools to resolve conflicts between customizations and the upgrade, and provides information to help estimate time for upgrades to other instances.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Monitor an upgrade to an instance, Upgrade Monitor module: Upgrade an individual instance, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Summary Report

This report summarizes the actions taken, provides tools to resolve conflicts between customizations and the upgrade, and provides information to help estimate time for upgrades to other instances.

![Top section of upgrade summary report](../image/upgrade-summary-02-small.png "Upgrade Summary Report: Database Upgrade Highlights")

<table><thead><tr><th>

Screen element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From version

</td><td>

Previous version of the instance

</td></tr><tr><td>

To version

</td><td>

Upgraded version of the instance

</td></tr><tr><td>

Started

</td><td>

When the upgrade process started

</td></tr><tr><td>

Finished

</td><td>

When the upgrade process finished

</td></tr><tr><td>

Duration

</td><td>

How long the upgrade process took

</td></tr><tr><td>

Skipped

</td><td>

In the example, `24 Skipped of 7016 changes` reads as:

-   **24 Skipped** - Total number of customizations that were skipped, skipped manual merge, or skipped in error, and the file changed in the distribution since the last upgrade of the instance. These are the number of records the system did not upgrade because of conflicts between customizations and the upgrade.
-   **7016 Changes** - Total number of file changes in the distribution since the last upgrade of the instance, plus all inserts and deletes.

 **Note:** The manner in which upgrade records are counted was changed in the Jakarta release, which may render different record counts than in previous releases.

</td></tr><tr><td>

Review Skipped Updates

</td><td>

Click to reconcile conflicts that caused the system to skip some updates

</td></tr></tbody>
</table>## Node Upgrades

![Node Upgrades section of upgrade summary report](../image/upgrade-summary-03-small.png "Upgrade Summary Report: Node Upgrades")

The Node Upgrades section shows the status of the upgrade for each node in the instance. The color of the icon denotes the status, as illustrated by the legend \(key\) and to the right of the node icons. To see details about a node, position the cursor above the icon for that node. An arrow points to the node selected, and the information below the icons pertains to that node.

## Schema Changes to Clone-excluded Tables

![Schema Changes to Clone-excluded Tables section of upgrade summary report](../image/upgrade-summary-04-small.png "Upgrade Summary Report: Schema Changes to Clone-excluded tables")

The Schema Changes to Clone-excluded Tables section shows a list of tables affected by the upgrade that were clone-excluded when you cloned the production instance to this instance. Because clone-excluded tables are empty, upgrading them takes less time than upgrading those same tables on the production instance. To estimate how much longer the production upgrade takes, note the size of the clone-excluded tables on the production instance.

## Top 10 Fix Scripts by Duration

![Top 10 Fix Scripts by Duration section of upgrade summary report](../image/upgrade-summ-fix-scripts-small.png "Upgrade Summary Report: Top 10 Fix Scripts by Duration")

The Top 10 Fix Scripts by Duration helps you understand which fix scripts required the most time.

## Top 10 Schema Changes by Duration

![Top 10 Schema Changes by Duration section of upgrade summary report](../image/upgrade-summ-schema-changes-small.png "Upgrade Summary Report: Top 10 Schema Changes by Duration")

The Top 10 Schema Changes by Duration helps you understand which schema changes required the most time.

**Parent Topic:**[Monitor an upgrade to an instance](../task/monitor-upgrade-apply-upgrade.md)

