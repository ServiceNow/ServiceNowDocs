---
title: Combined Operational Technology Manager release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Operational Technology Manager from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-operationaltechnologymanager-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Operational Technology Manager release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Operational Technology Manager from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Technology Manager release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Technology Manager to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Operational Technology Manager.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Use Enhanced Access Control for OT](https://www.servicenow.com/docs/access?context=ot-enhanced-access-control&family=zurich&ft:locale=en-US)**

Enhanced Access Control for OT implements data filters, deny unless access control rules \(ACLs\), and ACL query rules to help promote system security.


-   **[Operational Technology Network Map](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&family=zurich&ft:locale=en-US)**

Use the OT network map available in the Industrial Workspace to view a site's subnets and the OT devices in each subnet.

-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&family=zurich&ft:locale=en-US)**

Leverage an enhanced OT user experience and make additional configurations for your OT devices with the following CMDB OT class model updates:

    -   The IP Network Subnets related list was added to IT devices in the OT view to show all the subnets the device is related to show IP Network subnets for the selected OT device.

This related list was also added to the following CMDB classes:

        -   cmdb\_ci\_display
        -   cmdb\_ci\_firewall\_network
        -   cmdb\_ci\_security
        -   cmdb\_ci\_ids\_network
        -   cmdb\_ci\_imaging
        -   cmdb\_ci\_unclassed\_hardware
        -   cmdb\_ci\_multimedia
        -   cmdb\_ci\_monitor\_control
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_computer
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_hardware
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_iot
        -   cmdb\_ci\_ip\_firewall
        -   cmdb\_ci\_ip\_router
        -   cmdb\_ci\_ip\_switch
        -   cmdb\_ci\_linux\_server
        -   cmdb\_ci\_monitor\_control
        -   cmdb\_ci\_netgear
        -   cmdb\_ci\_ot
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_printer
        -   cmdb\_ci\_protocol\_converter
        -   cmdb\_ci\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
        -   cmdb\_ci\_win\_server
    -   You can now view the OT device details for the following CMDB classes:
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_hyper\_v\_server
    -   Because the OT device details are included in the form view of the CMDB class table, the **OT device details** tab was removed for the following CMDB classes:
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
    -   Admins can edit the protection policy for an OT View rule for all CMDB classes.

-   **[About the Industrial Workspace page](https://www.servicenow.com/docs/access?context=view-installed-ot-applications&family=zurich&ft:locale=en-US)**

Use the About Industrial Workspace page on the ServiceNow AI Platform to view the OT applications and the versions that you have installed on your instance.

-   **[Search for a record in the Industrial Workspace](https://www.servicenow.com/docs/access?context=search-in-industrial-workspace&family=zurich&ft:locale=en-US)**

Search for CMDB tables in the Industrial Workspace to find CMDB related records. The search function was previously limited only to other Operational Technology records.

-   **[Check whether an OT device is virtual](https://www.servicenow.com/docs/access?context=ot-assets-form&family=zurich&ft:locale=en-US)**

Check whether an OT device is virtual using the **Is Virtual** field for OT devices in the following categories:

    -   OT Supervisory System
    -   OT Control System
    -   OT Field Devices
    -   Unclassed OT Devices
-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&family=zurich&ft:locale=en-US)**

Leverage an enhanced OT user experience and make additional configurations for your OT devices with the following CMDB OT class model updates:

    -   The OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table references the CMDB CI relationships \[cmdb\_rel\_ci\] table to support device-to-device connections on the OT network.
    -   The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\] and Firmware Install \[cmdb\_firmware\_install\] table references were added to the OT view on IT and OT classes.
    -   The Backup Storage Information \[cmdb\_backup\_storage\_information\] and Backup Job Execution History \[cmdb\_backup\_job\_execution\_history\] tables reference the CMDB CI relationships \[cmdb\_rel\_ci\] table to support backup management use cases.
-   **[Pre-import OT Worksheet Entry Review \(POWER\) tool updates](https://www.servicenow.com/docs/access?context=service-graph-connector-for-OT-excel&family=zurich&ft:locale=en-US)**

Import OT devices with distributed Microsoft Excel spreadsheets to help manage your OT system and its devices. The Pre-Import OT Worksheet Entry Review \(POWER\) tool includes the following new functionality:

    -   Improve validations with access to ISA sites using the cmdb\_ot\_isa\_viewer role that has been added to the ot\_staging\_user role needed for running validations.
    -   Upload, validate, and import Microsoft Excel spreadsheet data for the Service Graph Connector for Microsoft Excel by creating an import task and attaching the spreadsheet to the import task record.
-   **[Create remediation tasks for invalid staging records from an import task](https://www.servicenow.com/docs/access?context=create-remediation-task-for-validation-errors&family=zurich&ft:locale=en-US)**

After validating the imported staging records, create remediation tasks for invalid staging records directly in the import task record.


</td></tr><tr><td>

Australia

</td><td>

-   **[Use Enhanced Access Control for OT](https://www.servicenow.com/docs/access?context=ot-enhanced-access-control&family=australia&ft:locale=en-US)**

Enhanced Access Control for OT implements data filters, deny unless access control rules \(ACLs\), and ACL query rules to help promote system security.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Operational Technology Network Map](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&family=australia&ft:locale=en-US)**

Use the OT network map available in the Industrial Workspace to view the subnets of a site and the OT devices in each subnet.

-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&family=australia&ft:locale=en-US)**

Configure for your OT devices with the following CMDB OT class model updates:

    -   The IP Network Subnets related list was added to IT devices in the OT view. The list shows all subnets related to the device and IP Network subnets for the selected OT device.
    -   The IP Network Subnets related list was added to the following CMDB classes:

        -   cmdb\_ci\_display
        -   cmdb\_ci\_firewall\_network
        -   cmdb\_ci\_security
        -   cmdb\_ci\_ids\_network
        -   cmdb\_ci\_imaging
        -   cmdb\_ci\_unclassed\_hardware
        -   cmdb\_ci\_multimedia
        -   cmdb\_ci\_monitor\_control
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_computer
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_hardware
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_iot
        -   cmdb\_ci\_ip\_firewall
        -   cmdb\_ci\_ip\_router
        -   cmdb\_ci\_ip\_switch
        -   cmdb\_ci\_linux\_server
        -   cmdb\_ci\_monitor\_control
        -   cmdb\_ci\_netgear
        -   cmdb\_ci\_ot
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_printer
        -   cmdb\_ci\_protocol\_converter
        -   cmdb\_ci\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
        -   cmdb\_ci\_win\_server
    -   You can now view the OT device details for the following CMDB classes:
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_hyper\_v\_server
    -   Because the OT device details are included in the form view of the CMDB class table, the **OT device details** tab was removed for the following CMDB classes:
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
    -   Admins can edit the protection policy for an OT View rule for all CMDB classes.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Operational Technology Manager features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Use CMDB groups to add OT context to IT CIs](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&family=zurich&ft:locale=en-US)**

When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than 1 CMDB group.

-   **[Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&family=zurich&ft:locale=en-US)**

The Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run.

-   **[Admin role dependency](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=zurich&ft:locale=en-US)**

Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[IT Discovery for Operational Technology \(OT\) Networks](https://www.servicenow.com/docs/access?context=discovery-for-operational-technology&family=zurich&ft:locale=en-US)**

The Discovery for Operational Technology plugin has been renamed IT Discovery for OT Networks.

-   **[Operational Technology Manager roles](https://www.servicenow.com/docs/access?context=assign-operational-technology-manager-roles&family=zurich&ft:locale=en-US)**

The following changes have been made to Operational Technology Manager roles:

    -   Users assigned the Operational Technology Manager Editor \[cmdb\_ot\_editor\] role or Operational Technology Manager Admin \[cmdb\_ot\_admin\] role cannot edit IT configuration items \(CIs\). Users with these roles can only edit or delete OT CIs.
    -   Users who aren't assigned an OT role cannot view OT records in the following CMDB tables:
        -   IP Address \[cmdb\_ci\_ip\_address\]
        -   Network Adapter \[cmdb\_ci\_network\_adapter\]
        -   Serial Number \[cmdb\_serial\_number\]
    -   The Operational Technology Editor \[cmdb\_ot\_editor\] role contains the cmdb\_manual\_ci\_ire\_access role to support manually creating an OT CI in the Industrial Workspace.

</td></tr><tr><td>

Australia

</td><td>

-   **[Use CMDB groups to add OT context to IT CIs](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&family=australia&ft:locale=en-US)**

When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than one CMDB group.

-   **[Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&family=australia&ft:locale=en-US)**

The **Automated IT OT Bulk Contextualization - Using CMDB groups** scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run.

-   **[Admin role dependency](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US)**

Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Operational Technology Manager features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   The **New** button was removed from the following related lists for users with read-only access to a site:
    -   Network Adapters
    -   Memory Modules
    -   Software Installed
    -   IP Addresses

</td></tr><tr><td>

Australia

</td><td>

-   The **New** button was removed from the following related lists for users with read-only access to a site:
    -   Network Adapters
    -   Memory Modules
    -   Software Installed
    -   IP Addresses

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Operational Technology Manager features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

For the Service Graph Connector for Microsoft Excel, the following items were deprecated on the ServiceNow AI Platform:

-   The SG OT Excel Staging Task table
-   The Staging task reference on the SG OT Excel Staging table

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Operational Technology Manager.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Operational Technology Manager by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Operational Technology Manager by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Operational Technology Manager we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Operational Technology Manager we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Operational Technology Manager, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Operational Technology Manager we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Operational Technology Manager we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Help promote system security by using Enhanced Access Control for OT.
-   Get a deeper look into your OT network with the OT network map in the Industrial Workspace, where you can view a site, its subnets, and the OT devices in each subnet.
-   View the Operational Technology Manager \(OT\) device-to-device connections with additional information such as port and protocol values.
-   Review the OT applications and versions that you have installed on the About Industrial Workspace page.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.

 See [Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Help promote system security by using Enhanced Access Control for OT.
-   Get a deeper look into your OT network with the OT network map in the Industrial Workspace, where you can view a site, its subnets, and the OT devices in each subnet.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.

 See for [Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&family=australia&ft:locale=en-US) more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

