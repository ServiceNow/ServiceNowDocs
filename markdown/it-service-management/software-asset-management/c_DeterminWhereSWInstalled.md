---
title: Determine where software is installed using the legacy Software Asset Management plugin
description: When using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to determine where your software is installed, you must keep the following points in mind.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Determine where software is installed using the legacy Software Asset Management plugin

When using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to determine where your software is installed, you must keep the following points in mind.

-   The software instance no longer contains discovered information. The information previously went to the Software Instance \[cmdb\_software\_instance\] table, but now goes to the Software Installation \[cmdb\_sam\_sw\_install\] table. Because the table has changed, you must change your transform maps to point to the new table.
-   Models identified by a discovery tool are linked to software models.
-   Use grouping to obtain more specific information from a software counter.
-   Software installations link a computer with a software model \(via a discovery model\).

A discovery tool places the data it obtains into the Software Installation \[cmdb\_sam\_sw\_install\] table. All of the information can be seen in the Software Installations list and the individual Software Installation forms. When a record is created, the system analyzes the Discovery Model table and identifies five key points.

-   Publisher
-   Display name
-   Prod ID
-   Version
-   Revision

-   **[Find software on the network using the legacy Software Asset Management plugin](../task/t_FindingSoftwareOnTheNetwork.md)**  
After using a discovery tool, you can find a definitive list of all the software found on the network using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
-   **[Scan software installations with the system scheduler](c_ScanSWInstWithSysSched.md)**  
The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds a scheduled job for scanning software installations named **SAM License Counters** in **System Scheduler** &gt; **Scheduled Jobs**.

**Parent Topic:**[Legacy Software Asset Management plugin](c_SoftwareAssetManagement.md)

**Related topics**  


[Legacy Software Asset Management plugin Overview module](c_SWAssetMgmtOverviewMod.md)

[Legacy Software Asset Management plugin setup process](c_SetupProcess.md)

[Software licenses in the legacy Software Asset Management plugin](c_SoftwareLicenses.md)

[Manage software models using the legacy Software Asset Management plugin](../task/t_ManagingSoftwareModels.md)

[License calculations with the legacy Software Asset Management plugin](c_UseLicenseCalculations.md)

[Software discovery models in the legacy Software Asset Management plugin](c_UsingSoftwareDiscoveryModels.md)

[Legacy Software License Compliance Checker](c_SoftwareLicenseComplianceChecker.md)

[Software license reconciliation counters for the legacy Software Asset Management plugin](c_UseCountersSWLicenseReconcil.md)

[Legacy IBM PVU Process Pack](c_IBMPVUProcessPack.md)

[Software contracts for the legacy Software Asset Management plugin](c_SoftwareContracts.md)

[Legacy Oracle process pack](c_OracleProcessPack.md)

