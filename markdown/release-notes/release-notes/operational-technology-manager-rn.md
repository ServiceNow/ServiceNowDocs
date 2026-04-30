---
title: Operational Technology Manager release notes
description: The ServiceNow Operational Technology Manager application enables you to aggregate Operational Technology \(OT\) device data from multiple sources so that you can build the foundational data relationships in the Industrial solution. Operational Technology Manager was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-21"
reading_time_minutes: 7
---

# Operational Technology Manager release notes

The ServiceNow® Operational Technology Manager application enables you to aggregate Operational Technology \(OT\) device data from multiple sources so that you can build the foundational data relationships in the Industrial solution. Operational Technology Manager was enhanced and updated in the Xanadu release.

## Operational Technology Manager highlights for the Xanadu release

-   Track your OT device data with the new Operational Technology Visibility dashboard.
-   Group OT devices using CMDB groups to support non-CMDB tables that must be converted from IT to OT.
-   Compare sites by key metrics in the Industrial Workspace using the OT Progress Scorecard.
-   Track tasks related to your OT system on the OT Action-Oriented Landing Page in the Industrial Workspace.
-   Map IP addresses to OT devices through the SyncIPAddressToOT scheduled job.
-   Use the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.
-   Use the updates and UI enhancements for the Pre-import OT Worksheet Entry Review \(POWER\) tool to help import and classify your OT device data.

See [Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US) for more information.

**Important:** Operational Technology Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Operational Technology Visibility dashboard](https://www.servicenow.com/docs/access?context=ot-manager-dashboard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Track your OT data across different sites with the Operational Technology Visibility dashboard available in the Industrial Workspace.

-   **[Automatic conversion of IT to OT devices using CMDB groups](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Use CMDB groups to group IT configuration items \(CIs\) based on additional information, such as software installed, so that you can convert the CIs to OT devices.

-   **[Mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Identify the equipment model entity that your OT devices are mapped to in the Industrial Workspace and help group your device data by equipment model entity.

-   **[Important actions configuration on the OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=configure-order-important-actions-aolp&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Configure the OT Action-Oriented Landing Page by using the **Sort items** field for your important actions.

-   **[OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=oper-tech-task-oriented-landing-page&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Track critical tasks related to your OT network on the OT Action-Oriented Landing Page in the Industrial Workspace. This landing page provides a big-picture view of your site and business unit data, and it calls out important actions that the signed-in user must prioritize.

-   **[Operational Technology Progress Scorecard](https://www.servicenow.com/docs/access?context=ot-progress-scorecard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Compare your sites by their key metrics with the OT Progress Scorecard in the Industrial Workspace. To access the OT Progress Scorecard, you must have the OT Progress Scorecard viewer \(ot\_progress\_scorecard\_viewer\) role.

-   **[Redirection to different pages in the Industrial Workspace](https://www.servicenow.com/docs/access?context=industrial-workspace-homepage-destination-rules&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Get redirected to different pages in Industrial Workspace depending on your assigned roles with the new homepage destination rules. This redirection helps you gain access to the data that you need.

-   **[Map IP addresses to OT devices through the SyncIPAddressToOT scheduled job](https://www.servicenow.com/docs/access?context=map-ip-addresses-to-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Use the `SyncIPAddressToOT` scheduled job to update and synchronize the IP address information for all the available OT devices. The scheduled job acquires the IP address information from the IP address \[cmdb\_ci\_ip\_address\] table and adds it to the **IP address** field of the Configuration Item \(CI\).

-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Utilize an enhanced OT user experience and make additional configurations with the following CMDB OT class model updates:

    -   Product Instance Identifier was added as an identifier for the OT Identification Rule.
    -   The OT backup management model was added to help you store multiple backups against a configuration item.
    -   Firmware Installation \[cmdb\_firmware\_install\], Key Value \[cmdb\_key\_value\], and Software Instance \[cmdb\_software\_instance\] tables were added as a related entry for OT classes.
    -   The **ire\_criterion\_attribute** attribute was added to the OT Entity \[cmdb\_ot\_entity\] table to act as a criterion attribute for an OT entity-related entry.
    -   Optional conditions to filter the records during identification and reconciliation were added to the OT identification rules.
    -   The OT Class Mapping Template \[ot\_class\_mapping\_template\] table was introduced to capture class mappings used for Service Graph Connectors.
    -   Required conditions were added under **Advanced Configuration** that must be met for lookup identification rules.
    -   Industrial printer \(industrial\_printer\) was added as an OT device type.
    -   The Quality Inspection Control System \[cmdb\_ci\_ot\_qics\] class represents the control systems that assist in quality and inspection functions. This new class is a child class of the OT Control System \[cmdb\_ci\_ot\_control\] class.
    -   The Backup Storage Information \[cmdb\_backup\_storage\_information\] class helps manage backups of your OT device data.
    -   The OT System Service \[cmdb\_ci\_ot\_system\_service\] class can model OT systems and their related software, hardware, and communication network components, such as a Distributed Control System \(DCS\).
    -   You can now bulk-validate NIDS records from the list view instead of validating each NIDS record individually.
-   **[Pre-import OT Worksheet Entry Review \(POWER\) tool](https://www.servicenow.com/docs/access?context=service-graph-connector-for-OT-excel&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Use distributed Microsoft Excel spreadsheets to import OT devices for better manageability of your OT system and its devices. The POWER tool includes the following new features:

    -   Firmware Installation records can be created when a firmware version is available.
    -   OT entity update issues can be resolved through the Service Graph Connector for Microsoft Excel.
    -   The new Industrial Core \[com.sn\_ot\_core\] plugin is required for class mapping when using the Service Graph Connector for Microsoft Excel.
    -   Supports the import and classification of the Quality Inspection Control System \[cmdb\_ci\_ot\_qics\] class. If you manually create an OT device in the SG-OT Excel Staging Table, the Quality Inspection Control System class is an option in the **What is the type of OT device?** task.
    -   Supports capturing the Backup Storage Information \[cmdb\_backup\_storage\_information\] class attributes on the staging table, staging table form, and the ETL.
    -   Maps the **Status** field in a staging table record to the **Life Cycle Stage** and **Life Cycle Status** fields on a configuration item \(CI\) record. The **Status** field no longer maps to the **Install Status** field on a CI record.
    -   Creates assets in the Industrial product model category for OT class devices. This enables compatibility with the Enterprise Asset Management product for full lifecycle management of OT class devices.

## UI changes

-   **[Request chart in the OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=oper-tech-task-oriented-landing-page&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    A chart for OT requests was added to the OT Action-Oriented Landing Page so you can track your requests in the Industrial Workspace.

-   **[Sort items field in the OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=oper-tech-task-oriented-landing-page&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The **Sort items** field was added to the OT Action-Oriented Landing Page under the **Important Actions** section.

-   **[Mapped Equipment Model Entity column](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The Mapped Equipment Model Entity column was added to the Industrial Workspace and ServiceNow AI Platform list views for OT devices. Use this column to identify the equipment model entity an OT device is mapped to.

-   **[Dashboard Library button](https://www.servicenow.com/docs/access?context=exploring-industrial-workspace&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The Dashboard Library icon \(![Dashboard Library icon](../../product/mftg-manufacturing-ot-vulnerability-response/image/dashboards-icon.png)\) was added to the Industrial Workspace and contains the available dashboards for Operational Technology, including the Operational Technology Visibility dashboard.

-   **[Site filter on the Operational Technology Visibility dashboard](https://www.servicenow.com/docs/access?context=ot-devices-dashboard-filters-vr&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    A site filter was added to the Operational Technology Visibility in the Industrial Workspace so you can filter the displayed data by a chosen site.

-   **[New home page in the Industrial Workspace](https://www.servicenow.com/docs/access?context=oper-tech-task-oriented-landing-page&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The OT Action-Oriented Landing Page is the new the home page of the Industrial Workspace.


## Changed in this release

-   **[OT Devices tab data](https://www.servicenow.com/docs/access?context=ot-manager-dashboard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The following data available in the **OT Devices** tab of the OT Manager dashboard has been moved to the Operational Technology Visibility dashboard.

    -   New OT devices discovered
    -   Inactive OT devices
    -   OT Devices overview
        -   Total CMDB OT devices
        -   Unclassed OT devices
        -   Unassigned OT devices
        -   Unmapped OT devices
    -   OT devices by category
        -   Supervisory systems
        -   Control systems
        -   Field devices
        -   Computers and servers
        -   Network Gear
        -   Industrial IoT
    -   OT devices by Purdue level
    -   OT devices by type \(Top Level\)
    -   OT devices by manufacturer \(Top Level\)
    -   OT devices by criticality

## Removed in this release

-   The **New** button has been removed from the **All OT Devices** list view and its corresponding list views.
-   The **New** button has been removed from the Equipment Model Entities related list in the Quality Inspection Control System \[cmdb\_ci\_ot\_qics\] form.

## Deprecations

-   The OT Manager dashboard is no longer available in the Industrial Workspace.
-   Starting with the Yokohama release, Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## Activation information

Install Operational Technology Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The Operational Technology Manager application automatically installs the latest version of the Operational Technology \(OT\) extension classes, available in the CMDB CI Class Models application in the ServiceNow Store.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

