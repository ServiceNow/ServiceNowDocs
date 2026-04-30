---
title: Operational Technology Manager release notes
description: The ServiceNow Operational Technology Manager application enables you to aggregate Operational Technology device data from multiple sources so you can build foundational data relationships in the Industrial solution. Operational Technology Manager was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
---

# Operational Technology Manager release notes

The ServiceNow® Operational Technology Manager application enables you to aggregate Operational Technology device data from multiple sources so you can build foundational data relationships in the Industrial solution. Operational Technology Manager was enhanced and updated in the Zurich release.

## Operational Technology Manager highlights for the Zurich release

-   Get a deeper look into your OT network with the OT network map in the Industrial Workspace, where you can view a site, its subnets, and the OT devices in each subnet.
-   View the Operational Technology Manager \(OT\) device-to-device connections with additional information such as port and protocol values.
-   Review the OT applications and versions that you have installed on the About Industrial Workspace page.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.
-   Improve the processes for importing and classifying your OT device data with updates and UI enhancements for the Pre-import OT Worksheet Entry Review \(POWER\) tool.

See [Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

**Important:** Operational Technology Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Operational Technology Network Map](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Use the OT network map available in the Industrial Workspace to view a site's subnets and the OT devices in each subnet.

-   **[About the Industrial Workspace page](https://www.servicenow.com/docs/access?context=view-installed-ot-applications&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Use the About Industrial Workspace page on the ServiceNow AI Platform to view the OT applications and the versions that you have installed on your instance.

-   **[Search for a record in the Industrial Workspace](https://www.servicenow.com/docs/access?context=search-in-industrial-workspace&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Search for CMDB tables in the Industrial Workspace to find CMDB related records. The search function was previously limited only to other Operational Technology records.

-   **[Check whether an OT device is virtual](https://www.servicenow.com/docs/access?context=ot-assets-form&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Check whether an OT device is virtual using the **Is Virtual** field for OT devices in the following categories:

    -   OT Supervisory System
    -   OT Control System
    -   OT Field Devices
    -   Unclassed OT Devices
-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

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
    -   The **OT device details** tab was removed for the following CMDB classes because the OT device details are included in the form view of the CMDB class table:
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
    -   Users assigned the admin role can edit the protection policy for an OT View rule for all CMDB classes.
    -   The OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table references the CMDB CI relationships \[cmdb\_rel\_ci\] table to support device-to-device connections on the OT network.
    -   The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\] and Firmware Install \[cmdb\_firmware\_install\] table references were added to the OT view on IT and OT classes.
    -   The Backup Storage Information \[cmdb\_backup\_storage\_information\] and Backup Job Execution History \[cmdb\_backup\_job\_execution\_history\] tables reference the CMDB CI relationships \[cmdb\_rel\_ci\] table to support backup management use cases.
-   **[Pre-import OT Worksheet Entry Review \(POWER\) tool updates](https://www.servicenow.com/docs/access?context=service-graph-connector-for-OT-excel&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Import OT devices with distributed Microsoft Excel spreadsheets to help manage your OT system and its devices. The Pre-Import OT Worksheet Entry Review \(POWER\) tool includes the following new functionality:

    -   Improve validations with access to ISA sites using the cmdb\_ot\_isa\_viewer role that has been added to the ot\_staging\_user role needed for running validations.
    -   Upload, validate, and import Microsoft Excel spreadsheet data for the Service Graph Connector for Microsoft Excel by creating an import task and attaching the spreadsheet to the import task record.
-   **[Create remediation tasks for invalid staging records from an import task](https://www.servicenow.com/docs/access?context=create-remediation-task-for-validation-errors&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    After validating the imported staging records, create remediation tasks for invalid staging records directly in the import task record.


## UI changes

-   **[Automated IT OT Bulk Conversion name change](https://www.servicenow.com/docs/access?context=automatically-convert-it-records-to-ot-devices&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Automated IT OT Bulk Conversion was replaced with Automated IT OT Bulk Contextualization on the ServiceNow AI Platform.

-   **[Banner messages for the Bulk Update Ruleset for Reassigning IT to OT feature](https://www.servicenow.com/docs/access?context=automatically-convert-it-records-to-ot-devices&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    A banner message was modified during the Bulk Update Ruleset for Reassigning IT to OT feature process to reflect the correct information when you use this feature.

-   **[IP Network Subnets related list](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The IP Network Subnets list was added for OT devices so you can see all subnets the selected OT device is associated with.

-   **[VLAN related list](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The VLAN related list was added to the OT device form view to show the VLANs associated with a device.

-   **[OT device related items and related lists](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\], and Firmware Install \[cmdb\_firmware\_install\] related lists were added to the OT view on IT and OT classes to view the following information:

    -   Information related to the OT device populated through the integrations and captured as Key Value pairs.
    -   Software installed on the OT device if Software Asset Management isn't available.
    -   Firmware associated with the OT device.
    You can view these related lists on the ServiceNow AI Platform® and in the Industrial Workspace Admin.

-   **[OT Excel SGC - Import Task list module in the Industrial Workspace](https://www.servicenow.com/docs/access?context=create-import-task-excel-sgc&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The OT Excel SGC - Import Task list module has been added to the Industrial Workspace list view. From the available lists, you can access the import task functionality for the Service Graph Connector for Microsoft Excel.

-   **[OT Excel SGC - Remediation Task list module in the Industrial Workspace](https://www.servicenow.com/docs/access?context=create-remediation-task-for-validation-errors&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The OT Excel SGC - Remediation Task list module has been added to the Industrial Workspace list view. From the available lists, you can access the remediation task records created from an import task.

-   **[View and edit device to device connections](https://www.servicenow.com/docs/access?context=view-device-to-device-connections&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The Device to Device Connections list has been added to the OT Network menu available in the Industrial Workspace List view. You can view the device connections in detail using this list. Also, the Device to Device Connections related list was added to the **Related Records** tab on the OT device record in the ServiceNow AI Platform.

-   **[Is Virtual field for OT devices](https://www.servicenow.com/docs/access?context=ot-assets-form&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Identify whether an OT device is virtual through the **Is Virtual** field added to the OT device form in the Industrial Workspace.

-   **[OT Subnet Mappings related list](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The OT Subnets related list has been renamed OT Subnet Mappings in both the Industrial Workspace and the ServiceNow AI Platform when viewing an OT device record.

-   **[__Manufacturer__ and __Model Number__ fields](https://www.servicenow.com/docs/access?context=ot-assets-form&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The **Manufacturer** and **Model Number** fields have been removed from the OT device list and form views on both the ServiceNow AI Platform® and in the Industrial Workspace.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Use CMDB groups to add OT context to IT CIs](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than 1 CMDB group.

-   **[Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run.

-   **Admin role dependency**

    Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[IT Discovery for Operational Technology \(OT\) Networks](https://www.servicenow.com/docs/access?context=discovery-for-operational-technology&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The Discovery for Operational Technology plugin has been renamed IT Discovery for OT Networks.

-   **[Operational Technology Manager roles](https://www.servicenow.com/docs/access?context=assign-operational-technology-manager-roles&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The following changes have been made to Operational Technology Manager roles:

    -   Users assigned the Operational Technology Manager Editor \[cmdb\_ot\_editor\] role or Operational Technology Manager Admin \[cmdb\_ot\_admin\] role cannot edit IT configuration items \(CIs\). Users with these roles can only edit or delete OT CIs.
    -   Users who aren't assigned an OT role cannot view OT records in the following CMDB tables:
        -   IP Address \[cmdb\_ci\_ip\_address\]
        -   Network Adapter \[cmdb\_ci\_network\_adapter\]
        -   Serial Number \[cmdb\_serial\_number\]
    -   The Operational Technology Editor \[cmdb\_ot\_editor\] role contains the cmdb\_manual\_ci\_ire\_access role to support manually creating an OT CI in the Industrial Workspace.

## Removed in this release

-   The **New** button was removed from the following related lists for users with read-only access to a site:
    -   Network Adapters
    -   Memory Modules
    -   Software Installed
    -   IP Addresses

## Deprecations

For the Service Graph Connector for Microsoft Excel, the following items were deprecated on the ServiceNow AI Platform:

-   The SG OT Excel Staging Task table
-   The Staging task reference on the SG OT Excel Staging table

## Activation information

Install Operational Technology Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The CMDB CI Class Models store application enables Operational Technology Manager to import and classify device data in ServiceNow. The Operational Technology Manager application automatically installs the latest version of the Operational Technology \(OT\) extension classes, available in the CMDB CI Class Models application in the ServiceNow Store.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

