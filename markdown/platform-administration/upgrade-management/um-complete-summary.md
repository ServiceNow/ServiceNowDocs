---
title: Upgrade Summary Report
description: The Upgrade Summary report summarizes the actions taken, provides tools to resolve conflicts between customizations and changes that are part of the upgrade, and provides information to help estimate time for upgrades to other instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/upgrade-management/um-complete-summary.html
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Monitor an upgrade to an instance, Upgrade Monitor tool in Upgrade Console, Upgrade Console tools, Use, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Summary Report

The Upgrade Summary report summarizes the actions taken, provides tools to resolve conflicts between customizations and changes that are part of the upgrade, and provides information to help estimate time for upgrades to other instances.

\[Omitted image "uc-complete-summary1.png"\] Alt text: Image showing summary report of the recently completed upgrade

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

\[Omitted image "uc-skipped-records.png"\] Alt text: Image showing Skipped Records in the Upgrade Summary Report

<table id="table_ghc_ycq_slb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Total record changes

</td><td>

Total number of records that have changed since the previous upgrade version.**Review changes**: List of records that have changed can be reviewed. See [System Upgrade form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-system-upgrades-form.md) for more details.

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
</table>**Note:** You can click **Skipped Record VTB** to view the resolution status of the current upgrade with skipped records using the visual task board \(VTB\) view. See [Skipped Records visual task board \(VTB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-vtb-history.md) for more information.

## Node Upgrades

\[Omitted image "uc-node-upgrades.png"\] Alt text: Image showing Node Upgrades in the Upgrade Summary Report

The Node Upgrades section shows the status of the upgrade for each node in the instance. The color of the icon denotes the status, as illustrated by the legend \(key\) and to the right of the node icons. To see details about a node, position the cursor above the icon for that node. An arrow points to the node selected, and the information below the icons pertains to that node.

## Application Upgrade Status

\[Omitted image "uc-application-status.png"\] Alt text: Application Upgrade Status.

You can view the list of installed and upgraded applications during an upgrade. It also lists the applications that failed to install during the process.

**Note:** The **All applications are on the latest versions** message shows up only when all the applications are on their latest versions.

\[Omitted image "uc-all-apps.png"\] Alt text: Installed and upgraded applications.You can view the first 10 applications that were installed during the upgrade. Select **View all application details** to view the information about all the installed, upgraded, and failed applications on the Upgrade App Version Histories table.

**Note:** You can select any of the application links to go to its form view. Select **Go to application** on the form view to go to the application sys record.

The following message shows up if you have selected any of the failed applications link.\[Omitted image "uc-failed-app-msg.png"\] Alt text: Application upgrade failure message.

## Schema Changes to Clone-excluded Tables

\[Omitted image "uc-schema-changes-clone.png"\] Alt text: Image showing Schema Changes to Clone-excluded Tables in the Upgrade Summary Report

The Schema Changes to Clone-excluded Tables section shows a list of tables affected by the upgrade that were clone-excluded when you cloned the production instance to this instance. Because clone-excluded tables are empty, upgrading them takes less time than upgrading those same tables on the production instance. To estimate how much longer the production upgrade takes, note the size of the clone-excluded tables on the production instance.

## Top 10 Fix Scripts by Duration

\[Omitted image "uc-fix-script-duration.png"\] Alt text: Image showing Top 10 Fix Scripts by Duration in the Upgrade Summary Report

The Top 10 Fix Scripts by Duration helps you understand which fix scripts required the most time.

## Top 10 Schema Changes by Duration

\[Omitted image "uc-schema-changes-duration.png"\] Alt text: Image showing Top 10 Schema Changes by Duration in the Upgrade Summary Report

The Top 10 Schema Changes by Duration helps you understand which schema changes required the most time.

## Top 10 Plugins by Duration

\[Omitted image ""\] Alt text:

The Top 10 Plugins by Duration helps you see the plugins that required the most time. Click **View all plugin duration** to see the **System Upgrade Metrics** list filtered by current sys upgrade history log and sorted by duration. See [View loaded files for a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-view-loaded-files-plugin.md) for more information.

-   **[View loaded files for a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-view-loaded-files-plugin.md)**  
Get a related list view of all the files loaded for a plugin by clicking **View all plugin duration**.

**Parent Topic:**[Monitor an upgrade to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-monitor-instance-upgrade.md)

