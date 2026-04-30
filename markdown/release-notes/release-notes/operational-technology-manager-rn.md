---
title: Operational Technology Manager release notes
description: The ServiceNow Operational Technology Manager application enables you to aggregate Operational Technology \(OT\) device data from multiple sources so that you can build the foundational data relationships in the Industrial solution. Operational Technology Manager was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 10
---

# Operational Technology Manager release notes

The ServiceNow® Operational Technology Manager application enables you to aggregate Operational Technology \(OT\) device data from multiple sources so that you can build the foundational data relationships in the Industrial solution. Operational Technology Manager was enhanced and updated in the Yokohama release.

## Operational Technology Manager highlights for the Yokohama release

-   View the Operational Technology Manager \(OT\) device-to-device connections with additional information such as port and protocol values.
-   Review the OT applications and versions that you have installed on the About Industrial Workspace page.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.
-   Track your OT device data with the new Operational Technology Visibility dashboard.
-   Group OT devices using CMDB groups to support non-CMDB tables that must be converted from IT to OT.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.
-   Improve the processes for importing and classifying your OT device data with updates and UI enhancements for the Pre-import OT Worksheet Entry Review \(POWER\) tool.

See [Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

**Important:** Operational Technology Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[About the Industrial Workspace page](https://www.servicenow.com/docs/access?context=view-installed-ot-applications&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Use the About Industrial Workspace page on the ServiceNow AI Platform to view the OT applications and the versions that you have installed on your instance.

-   **[Search for a record in the Industrial Workspace](https://www.servicenow.com/docs/access?context=search-in-industrial-workspace&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Search for CMDB tables in the Industrial Workspace to find CMDB related records. The search function was previously limited only to other Operational Technology records.

-   **[Check whether an OT device is virtual](https://www.servicenow.com/docs/access?context=ot-assets-form&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Check whether an OT device is virtual using the **Is Virtual** field for OT devices in the following categories:

    -   OT Supervisory System
    -   OT Control System
    -   OT Field Devices
    -   Unclassed OT Devices
-   **[Create remediation tasks for invalid staging records from an import task](https://www.servicenow.com/docs/access?context=create-remediation-task-for-validation-errors&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    After validating the imported staging records, create remediation tasks for invalid staging records directly in the import task record.

-   **[Operational Technology Visibility dashboard](https://www.servicenow.com/docs/access?context=ot-manager-dashboard&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Track your OT data across different sites with the Operational Technology Visibility dashboard available in the Industrial Workspace.


-   **[Automatic conversion of IT to OT devices using CMDB groups](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Use CMDB groups to group IT configuration items \(CIs\) based on additional information, such as software installed, so that you can convert the CIs to OT devices.

-   **[Mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Identify the equipment model entity that your OT devices are mapped to in the Industrial Workspace and help group your device data by equipment model entity.


-   **[Important actions configuration on the OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=configure-order-important-actions-aolp&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Configure the OT Action-Oriented Landing Page by using the **Sort items** field for your important actions.


-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Leverage an enhanced OT user experience and make additional configurations for your OT devices with the following CMDB OT class model updates:

    -   The OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table references the CMDB CI relationships \[cmdb\_rel\_ci\] table to support device-to-device connections on the OT network.
    -   The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\] and Firmware Install \[cmdb\_firmware\_install\] table references were added to the OT view on IT and OT classes.
    -   The Backup Storage Information \[cmdb\_backup\_storage\_information\] and Backup Job Execution History \[cmdb\_backup\_job\_execution\_history\] tables reference the CMDB CI relationships \[cmdb\_rel\_ci\] table to support backup management use cases.
    -   Product Instance Identifier was added as an identifier for the OT Identification Rule.
    -   The OT backup management model was added to help you store multiple backups against a configuration item.
    -   Firmware Installation \[cmdb\_firmware\_install\], Key Value \[cmdb\_key\_value\], and Software Instance \[cmdb\_software\_instance\] tables were added as a related entry for OT classes.
    -   The **ire\_criterion\_attribute** attribute was added to the OT Entity \[cmdb\_ot\_entity\] table to act as a criterion attribute for an OT entity-related entry.
    -   Optional conditions to filter the records during identification and reconciliation were added to the OT identification rules.
    -   The OT Class Mapping Template \[ot\_class\_mapping\_template\] table was introduced to capture class mappings used for Service Graph Connectors.
    -   Required conditions were added under **Advanced Configuration** that must be met for lookup identification rules.
    -   Industrial printer \(industrial\_printer\) was added as an OT device type.
-   **[Pre-import OT Worksheet Entry Review \(POWER\) tool updates](https://www.servicenow.com/docs/access?context=service-graph-connector-for-OT-excel&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Import OT devices with distributed Microsoft Excel spreadsheets to help manage your OT system and its devices. The Pre-Import OT Worksheet Entry Review \(POWER\) tool includes the following new functionality:

    -   Improve validations with access to ISA sites using the cmdb\_ot\_isa\_viewer role that has been added to the ot\_staging\_user role needed for running validations.
    -   Upload, validate, and import Microsoft Excel spreadsheet data for the Service Graph Connector for Microsoft Excel by creating an import task and attaching the spreadsheet to the import task record.
    -   Firmware Installation records can be created when a firmware version is available.
    -   OT entity update issues can be resolved through the Service Graph Connector for Microsoft Excel.
    -   The new Industrial Core plugin \(com.sn\_ot\_core\) is required for class mapping when using the Service Graph Connector for Microsoft Excel.

## UI changes

-   **[OT device related items and related lists](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\], and Firmware Install \[cmdb\_firmware\_install\] related lists were added to the OT view on IT and OT classes to view the following information:

    -   Information related to the OT device populated through the integrations and captured as Key Value pairs.
    -   Software installed on the OT device if Software Asset Management isn't available.
    -   Firmware associated with the OT device.
    You can view these related lists on the ServiceNow AI Platform® and in the Industrial Workspace Admin.

-   **[OT Excel SGC - Import Task list module in the Industrial Workspace](https://www.servicenow.com/docs/access?context=create-import-task-excel-sgc&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The OT Excel SGC - Import Task list module has been added to the Industrial Workspace list view. From the available lists, you can access the import task functionality for the Service Graph Connector for Microsoft Excel.

-   **[OT Excel SGC - Remediation Task list module in the Industrial Workspace](https://www.servicenow.com/docs/access?context=create-remediation-task-for-validation-errors&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The OT Excel SGC - Remediation Task list module has been added to the Industrial Workspace list view. From the available lists, you can access the remediation task records created from an import task.

-   **[View and edit device to device connections](https://www.servicenow.com/docs/access?context=view-device-to-device-connections&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Device to Device Connections list has been added to the OT Network menu available in the Industrial Workspace List view. You can view the device connections in detail using this list. Also, the Device to Device Connections related list was added to the **Related Records** tab on the OT device record in the ServiceNow AI Platform.

-   **[Is Virtual field for OT devices](https://www.servicenow.com/docs/access?context=ot-assets-form&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Identify whether an OT device is virtual through the **Is Virtual** field added to the OT device form in the Industrial Workspace.

-   **[OT Subnet Mappings related list](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The OT Subnets related list has been renamed OT Subnet Mappings in both the Industrial Workspace and the ServiceNow AI Platform when viewing an OT device record.

-   **[__Manufacturer__ and __Model Number__ fields](https://www.servicenow.com/docs/access?context=ot-assets-form&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The **Manufacturer** and **Model Number** fields have been removed from the OT device list and form views on both the ServiceNow AI Platform® and in the Industrial Workspace.

-   **[Request chart in the OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=oper-tech-task-oriented-landing-page&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    A chart for OT requests was added to the OT Action-Oriented Landing Page so you can track your requests in the Industrial Workspace.

-   **[Sort items field in the OT Action-Oriented Landing Page](https://www.servicenow.com/docs/access?context=oper-tech-task-oriented-landing-page&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The **Sort items** field was added to the OT Action-Oriented Landing Page under the **Important Actions** section.

-   **[Mapped Equipment Model Entity column](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Mapped Equipment Model Entity column was added to the Industrial Workspace and ServiceNow AI Platform list views for OT devices. Use this column to identify the equipment model entity an OT device is mapped to.

-   **[Dashboard Library icon](https://www.servicenow.com/docs/access?context=exploring-industrial-workspace&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Dashboard Library icon \(![Dashboard Library icon](../../product/mftg-manufacturing-ot-vulnerability-response/image/dashboards-icon.png)\) was added to the Industrial Workspace and contains the available dashboards for Operational Technology, including the Operational Technology Visibility dashboard.

-   **[Site filter on the Operational Technology Visibility dashboard](https://www.servicenow.com/docs/access?context=ot-devices-dashboard-filters-vr&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    A site filter was added to the Operational Technology Visibility in the Industrial Workspace so you can filter the displayed data by a chosen site.


## Changed in this release

-   **[OT device related items and related lists](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\], and Firmware Install \[cmdb\_firmware\_install\] related lists were added to the OT view on IT and OT classes to view the following information:

    -   Information related to the OT device populated through the integrations and captured as Key Value pairs.
    -   Software installed on the OT device if Software Asset Management isn't available.
    -   Firmware associated with the OT device.
    You can view these related lists on the ServiceNow AI Platform® and in the Industrial Workspace Admin.

-   **[OT Excel SGC - Import Task list module in the Industrial Workspace](https://www.servicenow.com/docs/access?context=create-import-task-excel-sgc&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The OT Excel SGC - Import Task list module has been added to the Industrial Workspace list view. From the available lists, you can access the import task functionality for the Service Graph Connector for Microsoft Excel.

-   **[OT Excel SGC - Remediation Task list module in the Industrial Workspace](https://www.servicenow.com/docs/access?context=create-remediation-task-for-validation-errors&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The OT Excel SGC - Remediation Task list module has been added to the Industrial Workspace list view. From the available lists, you can access the remediation task records created from an import task.

-   **[View and edit device to device connections](https://www.servicenow.com/docs/access?context=view-device-to-device-connections&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Device to Device Connections list has been added to the OT Network menu available in the Industrial Workspace List view. You can view the device connections in detail using this list. Also, the Device to Device Connections related list was added to the **Related Records** tab on the OT device record in the ServiceNow AI Platform.

-   **[Is Virtual field for OT devices](https://www.servicenow.com/docs/access?context=ot-assets-form&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Identify whether an OT device is virtual through the **Is Virtual** field added to the OT device form in the Industrial Workspace.

-   **[OT Subnet Mappings related list](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The OT Subnets related list has been renamed OT Subnet Mappings in both the Industrial Workspace and the ServiceNow AI Platform when viewing an OT device record.

-   **[__Manufacturer__ and __Model Number__ fields](https://www.servicenow.com/docs/access?context=ot-assets-form&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The **Manufacturer** and **Model Number** fields have been removed from the OT device list and form views on both the ServiceNow AI Platform® and in the Industrial Workspace.

-   **[OT Devices tab data](https://www.servicenow.com/docs/access?context=ot-manager-dashboard&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

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

## Deprecations

-   For the Service Graph Connector for Microsoft Excel, the following items were deprecated on the ServiceNow AI Platform:
    -   The SG OT Excel Staging Task table
    -   The Staging task reference on the SG OT Excel Staging table
-   The OT Manager dashboard is no longer available in the Industrial Workspace.
-   Starting with the Yokohama release, Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## Activation information

Install Operational Technology Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    The CMDB CI Class Models store application enables Operational Technology Manager to import and classify device data in ServiceNow. The Operational Technology Manager application automatically installs the latest version of the Operational Technology \(OT\) extension classes, available in the CMDB CI Class Models application in the ServiceNow Store.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

