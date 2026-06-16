---
title: Operational Technology Manager release notes
description: Version history for the Operational Technology Manager application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-manufacturing-operational-tech-manager.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Operational Technology release notes, ServiceNow Store release notes]
---

# Operational Technology Manager release notes

Version history for the Operational Technology Manager application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.0 - June 2026**

    New: Certified for Australia Patch 3

-   **Version 3.1.0 - March 2026**
    -   New:
        -   Access the network map for your OT network in the Industrial Workspace
        -   The following CMDB OT class model updates have been added:
            -   The IP Network Subnets related list was added to IT devices in the OT view to show all the subnets the device is related to show IP Network subnets for the selected OT device
            -   You can now view the OT device details for cmdb\_ci\_esx\_server and cmdb\_ci\_hyper\_v\_server classes
            -   Users assigned the admin role can edit the protection policy for an OT View rule for all CMDB classes
        -   The Automated IT to OT Bulk Contextualization name was changed to Automated It to OT Bulk Conversion
        -   The VLAN related list was added for OT devices
        -   Certified for Australia
    -   Changed:
        -   When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than 1 CMDB group
        -   The Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run
-   **Version 3.0.0 - December 2025**
    -   Changed:
        -   Minor Platform enhancements and a defect fix
        -   Minor fix on Excel Template
-   **Version 2.0.9 - August 2025**
    -   New:
        -   Use the About Industrial Workspace page on the ServiceNow AI Platform to view the OT applications and the versions that you have installed on your instance.
        -   Search for CMDB tables in the Industrial Workspace to find CMDB related records. The search function was previously limited only to other Operational Technology records.
        -   Check whether an OT device is virtual using the Is Virtual field for OT devices in the following categories.
        -   CMDB OT class model updates:
            -   The OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table references the CMDB CI relationships \[cmdb\_rel\_ci\] table to support device-to-device connections on the OT network.
            -   The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\] and Firmware Install \[cmdb\_firmware\_install\] table references were added to the OT view on IT and OT classes.
            -   The Backup Storage Information \[cmdb\_backup\_storage\_information\] and Backup Job Execution History \[cmdb\_backup\_job\_execution\_history\] tables reference the CMDB CI relationships \[cmdb\_rel\_ci\] table to support backup management use cases.
        -   The Pre-Import OT Worksheet Entry Review \(POWER\) tool includes the following new functionality:
            -   Improve validations with access to ISA sites using the cmdb\_ot\_isa\_viewer role that has been added to the ot\_staging\_user role needed for running validations.
            -   Upload, validate, and import Microsoft Excel spreadsheet data for the Service Graph Connector for Microsoft Excel by creating an import task and attaching the spreadsheet to the import task record.
        -   After validating the imported staging records, create remediation tasks for invalid staging records directly in the import task record.
    -   Changed:
        -   The following changes have been made to Operational Technology Manager roles:
            -   Users assigned the Operational Technology Manager Editor \[cmdb\_ot\_editor\] role or Operational Technology Manager Admin \[cmdb\_ot\_admin\] role cannot edit IT configuration items \(CIs\). Users with these roles can only edit or delete OT CIs.
            -   Users who aren't assigned an OT role cannot view OT records in the following CMDB tables:
                -   IP Address \[cmdb\_ci\_ip\_address\]
                -   Network Adapter \[cmdb\_ci\_network\_adapter\]
                -   Serial Number \[cmdb\_serial\_number\]
            -   The Operational Technology Editor \[cmdb\_ot\_editor\] role contains the cmdb\_manual\_ci\_ire\_access role to support manually creating an OT CI in the Industrial Workspace.
        -   The Discovery for Operational Technology plugin has been renamed IT Discovery for OT Networks.
        -   The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\], and Firmware Install \[cmdb\_firmware\_install\] related lists were added to the OT view on IT and OT classes.
        -   The OT Excel SGC - Import Task list module has been added to the Industrial Workspace list view.
        -   The OT Excel SGC - Remediation Task list module has been added to the Industrial Workspace list view.
        -   The Device to Device Connections list has been added to the OT Network menu available in the Industrial Workspace List view. You can view the device connections in detail using this list. Also, the Device to Device Connections related list was added to the Related Records tab on the OT device record in the ServiceNow AI Platform.
        -   Identify whether an OT device is virtual through the Is Virtual field added to the OT device form in the Industrial Workspace.
        -   The OT Subnets related list has been renamed OT Subnet Mappings in both the Industrial Workspace and the ServiceNow AI Platform when viewing an OT device record.
        -   The Manufacturer and Model Number fields have been removed from the OT device list and form views on both the ServiceNow AI Platform and in the Industrial Workspace.
    -   Removed:
        -   For the Service Graph Connector for Microsoft Excel, the following items were deprecated on the ServiceNow AI Platform:
            -   The SG OT Excel Staging Task table
            -   The Staging task reference on the SG OT Excel Staging table
-   **Version 2.0.8 - May 2025**

    New: Updated with various bug fixes.

-   **Version 2.0.7 - February 2025**
    -   New:
        -   Track your OT device data with the new Operational Technology Visibility dashboard.
        -   Group OT devices using CMDB groups to support non-CMDB tables that need to be converted from IT to OT.
        -   Identify the equipment model entity your OT devices are mapped to help group your devices by equipment model entity.
        -   Use the improved Industrial Workspace to track and manage your OT device data.
        -   Use the Configuration Management Database \(CMDB\) OT class model updates and UI improvements.
        -   Use the updates and UI improvements for the Pre-import OT Worksheet Entry Review \(POWER\) tool to help import and classify your OT device data.
-   **Version 2.0.4 - November 2024**

    Fixed: Updated with various bug fixes.

-   **Version 2.0.2 - September 2024**
    -   New:
        -   Compare sites by key metrics in the Industrial Workspace using the OT Progress Scorecard
        -   Track tasks related to your OT system on the OT Action-Oriented Landing Page in the Industrial Workspace
        -   The OT Action-Oriented Landing Page has replaced the OT Manager dashboard as the home page of the Industrial Workspace
        -   Use the updates and UI improvements for the Pre-import OT Worksheet Entry Review \(POWER\) tool to help import and classify your OT device data
        -   Certified for Xanadu
-   **Version 2.0.1 - August 2024**
    -   Compare sites by key metrics in the Industrial Workspace using the OT Progress Scorecard
    -   Track tasks related to your OT system on the OT Action-Oriented Landing Page in the Industrial Workspace
    -   The OT Action-Oriented Landing Page has replaced the OT Manager dashboard as the home page of the Industrial Workspace
    -   Use the updates and UI improvements for the Pre-import OT Worksheet Entry Review \(POWER\) tool to help import and classify your OT device data
    -   Certified for Xanadu
-   **Version 1.1.10 - February 2024**
    -   Migrated landing page dashboard to PA to enable KPI trending
    -   Improved performance by splitting the landing page into OT devices landing page tab and OT vulnerabilities landing page tab.
    -   Added capability to filter sites on landing page dashboard by business unit
    -   Users can select single site, multiple sites, and "no site assigned" and landing page data refreshes immediately after the selection.
    -   The count of control modules is removed from control systems under OT devices landing page tab.
    -   OT asset has been renamed to OT device. This is reflected across all the list views, buttons etc.
    -   Certified for Washington DC
-   **Version 1.1.9 - August 2023**

    -   Certified for Vancouver
    -   Convert IT hardware to OT assets in a bulk edit
    -   Convert your OT assets to IT hardware devices in a bulk edit
    -   Firmware column was added to appropriate application menu list views under Operational Technology \(OT\) in the platform
    -   Module types were added to the Control module class: Local, Remote and Distributed.
    -   The External System URL related list was added to the Operational Technology \(OT\) view for Core IT classes.
    -   A Remote check box with yes or no options was added to the OT control module to differentiate the regular control modules from the Remote I/O.
    -   The OT display name field was added to the OT asset form and the All OT Assets list on the Industrial Workspace. The OT display name field is a user-friendly name that you can add to the OT asset record.
    Updates to the Service Graph Connector for OT \(Excel\):

    -   Preview the records that already exist in the CMDB. You can do this before you import OT asset records from the staging table to the CMDB to avoid merging or reconciling the duplicate records.
    -   Validation of Site field has been added on staging table.
-   **Version 1.1.8 - February 2023**
    -   New:
        -   Certified for Utah
        -   New role cmdb\_ot\_isa\_viewer\_all allows user read-only access to all equipment model entitiescmdb\_ot\_admin role now includes cmdb\_ot\_isa\_viewer\_all
-   **Version 1.1.7 - November 2022**
    -   Fixed:
        -   After filtering on a list with an OR condition, Remove filter is now available
        -   Manufacturing Workspace Landing Page now shows correct counts for ot\_viewer without a cmdb\_ot\_isa\_viewer role for OT assets not assigned to a site.
    -   Changed:
        -   Owns::Owned by relationship is created between OT control system and OT control module class OT assets when user creates an OT control module from the OT control module related list
-   **Version 1.1.6 - August 2022**
    -   New:
        -   Added staging table to facilitate Pre-import OT Worksheet Entry Review
        -   Added related lists on OT assets for OT Incidents and OT Vulnerable Items \(dependent on having respective plugins loaded\)
        -   Added timeline component to Manufacturing Workspace record form
        -   Now includes ISA Equipment Model plugin
-   **Version 1.1.5 - March 2022**

    New: Support for dark mode workspace experience

-   **Version 1.1.4 - February 2022**
    -   New:
        -   OT asset details moved to top of form in workspace view
        -   Equipment Model Entity related list added to OT asset forms
        -   New application menu to allow sorting and searching of OT assets by IP address
        -   Added IT Class to All OT Assets list view
        -   No longer automatically loads Discovery for Operational Technology plugin
-   **Version 1.1.2 - November 2021**
    -   Changed:
        -   Renamed application menu from Unclassified OT to Unclassed OT
        -   Relabeled landing page “Unclassified” single score to “Unclassed”

**Parent Topic:**[ServiceNow Store - Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-manufacturing-highlights.md)

