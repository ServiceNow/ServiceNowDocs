---
title: Legacy IBM PVU Process Pack
description: Processor Value Unit \(PVU\) is a unit of measurement defined by IBM to determine software licensing costs based on processor or server model.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Legacy IBM PVU Process Pack

Processor Value Unit \(PVU\) is a unit of measurement defined by IBM to determine software licensing costs based on processor or server model.

A processor is defined as each core on a socket. Each software package has a price defined as number of points or PVUs per core. For a complete explanation of IBM PVU licensing for distributed software, see [Processor Value Unit \[PVU\] licensing for Distributed Software](https://www-01.ibm.com/software/lotus/passportadvantage/pvu_licensing_for_customers.html) on the IBM website.

In the ServiceNow AI Platform, the concept of PVU is used by the legacy IBM PVU Process Pack, which is an add-on to the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin. This legacy process pack provides the ability to manage software licensed under the IBM Processor Value Units licensing model.

**Important:** The legacy IBM PVU Process Pack is not required for tracking and managing IBM PVU licenses through the Software Asset Management publisher pack for IBM, which is available as part of the Software Asset Management Professional \(com.snc.samp\) plugin. The IBM publisher pack includes all capabilities that are required for tracking and managing both full capacity and sub-capacity PVU and RVU licenses for your IBM products. See Software Asset Management publisher pack for IBM for more information on the IBM publisher pack.

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin Processor Definition Extension is automatically activated when the legacy IBM PVU Process Pack is activated. It provides data model support for processor definitions and is required by all legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin process packs.

**Note:** Oracle and Microsoft also use the concept of PVU, but have slightly different definitions.

-   **[Activate the legacy IBM PVU Process Pack](../task/t_ActivatingTheIBMPVUProcessPack.md)**  
The legacy Software Asset Management - IBM PVU Process Pack \(com.snc.sam.ibmpvu.pp\) plugin can no longer be activated upon request. If the legacy plugin has already been activated on your ServiceNow instance, you can continue to use the legacy IBM PVU Process Pack.
-   **[Validate legacy IBM PVU Process Pack requirements for associating software installations with PVU mappings](../task/t_ReqAssocSWInstToPVUMapping.md)**  
Meet the recommended requirements to ensure that you receive the highest quality results with PVU mapping.
-   **[IBM PVU mapping preparation for the legacy IBM PVU Process Pack](c_PreparingForIBMPVUMapping.md)**  
Most IBM PVU mapping and license checking for the legacy IBM PVU Process Pack is managed automatically.
-   **[Refresh your legacy Software Asset Management plugin processor definitions](../task/t_RefreshProcessorDefinitions.md)**  
After activating the legacy IBM PVU Process Pack, use the Refresh Processor Definitions module in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to create process definitions for existing computers in the Computer \[cmdb\_ci\_computer\] table.
-   **[Legacy Software Asset Management plugin processor definitions](../reference/r_ViewingProcessorDefinitions.md)**  
Processor definitions for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin are automatically derived from the information in the configuration item form for an item such as a computer or server.
-   **[View IBM PVU mappings for the legacy IBM PVU Process Pack](../task/t_ViewingIBMPVUMappings.md)**  
Every rule listed in the IBM PVU Table is represented by one PVU mapping record in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
-   **[Use software counters with the legacy IBM PVU Process Pack](../task/t_UseSWCountersCalcIBMPVULice.md)**  
To calculate IBM PVU licenses through the legacy IBM PVU Process Pack, you can create a software counter with the IBM PVU license type. For a given PVU software package, you only need to create the counter once and then it can be reused.
-   **[Installed with the legacy IBM PVU Process Pack](../reference/r_IWSWAssetMgmtIBMProcPack.md)**  
The following tables, fields, script includes, and business rules are installed with the legacy IBM PVU process pack.

**Parent Topic:**[Legacy Software Asset Management plugin](c_SoftwareAssetManagement.md)

**Related topics**  


[Legacy Software Asset Management plugin Overview module](c_SWAssetMgmtOverviewMod.md)

[Legacy Software Asset Management plugin setup process](c_SetupProcess.md)

[Determine where software is installed using the legacy Software Asset Management plugin](c_DeterminWhereSWInstalled.md)

[Software licenses in the legacy Software Asset Management plugin](c_SoftwareLicenses.md)

[Manage software models using the legacy Software Asset Management plugin](../task/t_ManagingSoftwareModels.md)

[License calculations with the legacy Software Asset Management plugin](c_UseLicenseCalculations.md)

[Software discovery models in the legacy Software Asset Management plugin](c_UsingSoftwareDiscoveryModels.md)

[Legacy Software License Compliance Checker](c_SoftwareLicenseComplianceChecker.md)

[Software license reconciliation counters for the legacy Software Asset Management plugin](c_UseCountersSWLicenseReconcil.md)

[Software contracts for the legacy Software Asset Management plugin](c_SoftwareContracts.md)

[Legacy Oracle process pack](c_OracleProcessPack.md)

