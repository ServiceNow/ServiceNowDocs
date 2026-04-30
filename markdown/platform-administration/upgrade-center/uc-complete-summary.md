---
title: Upgrade Summary Report
description: The Upgrade Summary report summarizes the actions taken, provides tools to resolve conflicts between customizations and changes that are part of the upgrade, and provides information to help estimate time for upgrades to other instances.
locale: en-US
release: xanadu
product: Upgrade Center
classification: upgrade-center
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Monitor an upgrade to an instance, Scheduling and monitoring an upgrade, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Summary Report

The Upgrade Summary report summarizes the actions taken, provides tools to resolve conflicts between customizations and changes that are part of the upgrade, and provides information to help estimate time for upgrades to other instances.

![Image showing summary report of the recently completed upgrade](../image/uc-complete-summary1.png)

<table id="table_b5b_p14_dlb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Upgraded version

</td><td>

Version to which the instance has been upgraded

</td></tr><tr><td>

Upgrade duration

</td><td>

Total time taken to make the upgrade

</td></tr><tr><td>

Find out what's new and changed

</td><td>

Links to view the new and changed features in the current upgrade version. The following three links show up.-   Problem fixes: Fixes that have been made since the last upgrade version
-   Personalized release notes: Release notes summary for the previewed version
-   Known error articles: Errors that have been identified but not yet resolved

</td></tr></tbody>
</table>## Skipped Records

![Image showing Skipped Records in the Upgrade Summary Report](../image/uc-skipped-records.png)

<table id="table_ghc_ycq_slb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Total record changes

</td><td>

Total number of records that have changed since the previous upgrade version.**Review changes**: List of records that have changed can be reviewed. See [System Upgrade form](uc-system-upgrades-form.md) for more details.

</td></tr><tr><td>

Skipped records

</td><td>

Skipped records to prevent your customizations from being overwritten. If customizations are found in some records during the upgrade, those records are skipped.As an admin, you can resolve each update that was skipped due to a customization. To resolve a skipped update, you can review the reason for each skipped record and then either retain the customization or revert the customization to the base system. If you choose to revert some of the customizations to the base version, those records are sent through the upgrade without getting skipped.

-   **Total**: Total skipped records
-   **To review**: Total skipped records that are yet to be reviewed
-   **Reviewed**: Total skipped records that have been reviewed

</td></tr><tr><td>

Skipped records by priority

</td><td>

ServiceNow prioritizes the skipped records based on the importance of the file types. The prioritization is done as follows:-   Priority 1 \(highest priority\): UI pages, UI macros, and more
-   Priority 2: Business Rules, Security ACLs, and more
-   Priority 3: Reports and more
-   Priority 4: Form Sections, Choice Sets, and more
-   Priority 5 \(lowest priority\): other

</td></tr><tr><td>

Skipped records by product

</td><td>

Skipped records are sorted by product names

</td></tr><tr><td>

Skipped records code changed/code unchanged

</td><td>

Skipped records are sorted depending on if there are changes in the code or not.

</td></tr></tbody>
</table>**Note:** You can click **Skipped Record VTB** to view the resolution status of the current upgrade with skipped records using the visual task board \(VTB\) view. See [Skipped Records visual task board \(VTB\)](../concept/uc-vtb-history.md) for more information.

## Node Upgrades

![Image showing Node Upgrades in the Upgrade Summary Report](../image/uc-node-upgrades.png)

The Node Upgrades section shows the status of the upgrade for each node in the instance. The color of the icon denotes the status, as illustrated by the legend \(key\) and to the right of the node icons. To see details about a node, position the cursor above the icon for that node. An arrow points to the node selected, and the information below the icons pertains to that node.

## Application Upgrade Status

![](../image/uc-application-status.png)

You can view the list of installed and upgraded applications during an upgrade. It also lists the applications that failed to install during the process.

**Note:** The **All applications are on the latest versions** message shows up only when all the applications are on their latest versions.

![](../image/uc-all-apps.png)You can view the first 10 applications that were installed during the upgrade. Select **View all application details** to view the information about all the installed, upgraded, and failed applications on the Upgrade App Version Histories table.

**Note:** You can select any of the application links to go to its form view. Select **Go to application** on the form view to go to the application sys record.

The following message shows up if you have selected any of the failed applications link.![](../image/uc-failed-app-msg.png)

## Schema Changes to Clone-excluded Tables

![Image showing Schema Changes to Clone-excluded Tables in the Upgrade Summary Report](../image/uc-schema-changes-clone.png)

The Schema Changes to Clone-excluded Tables section shows a list of tables affected by the upgrade that were clone-excluded when you cloned the production instance to this instance. Because clone-excluded tables are empty, upgrading them takes less time than upgrading those same tables on the production instance. To estimate how much longer the production upgrade takes, note the size of the clone-excluded tables on the production instance.

## Top 10 Fix Scripts by Duration

![Image showing Top 10 Fix Scripts by Duration in the Upgrade Summary Report](../image/uc-fix-script-duration.png)

The Top 10 Fix Scripts by Duration helps you understand which fix scripts required the most time.

## Top 10 Schema Changes by Duration

![Image showing Top 10 Schema Changes by Duration in the Upgrade Summary Report](../image/uc-schema-changes-duration.png)

The Top 10 Schema Changes by Duration helps you understand which schema changes required the most time.

## Top 10 Plugins by Duration

![]()

The Top 10 Plugins by Duration helps you see the plugins that required the most time. Click **View all plugin duration** to see the **System Upgrade Metrics** list filtered by current sys upgrade history log and sorted by duration. See [View loaded files for a plugin](../task/uc-view-loaded-files-plugin.md) for more information.

