---
title: Software discovery models in the legacy Software Asset Management plugin
description: Software discovery models in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin can be used to help normalize the software you own by analyzing and classifying models to reduce duplication.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software discovery models in the legacy Software Asset Management plugin

Software discovery models in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin can be used to help normalize the software you own by analyzing and classifying models to reduce duplication.

Software discovery models are stored in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table. There is a distinct difference between software models and software discovery models.

-   A software model is a specific version or configuration of software.
-   A software discovery model is a model created when Discovery runs and identifies software.

Software discovery models cannot be created manually. The ServiceNow platform uses any of the following field combinations to match the new software discovery model to an existing software model.

-   **Display Name**, **Publisher**, and **Version**
-   **Display Name** and **Version** if the **Publisher** field is empty
-   **Display Name** only if the **Publisher** and **Version** fields are empty

When analyzing version numbers, the ServiceNow platform always searches for an exact match first, but rounds down to a major version number if an exact match is not found. For example, if no match is found for version number 8.0.4, but version 8.0 is found, then version 8.0 is used in the **Software model** field.

-   **[Edit a software discovery model using the legacy Software Asset Management plugin](../task/t_EditingASoftwareDiscoveryModel.md)**  
You can edit only the **Software model** field and **Approved** check box on the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin Software Discovery Models form.
-   **[Automatically match to an existing model using the legacy Software Asset Management plugin](../task/t_AutoMatchExistingModel.md)**  
The automatic matching feature in the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin allows you to match a software discovery model to an existing software model.
-   **[Create new models using the legacy Software Asset Management plugin](../task/t_CreatingNewModels.md)**  
If the automatically generated software model is not correct or if the system cannot find a match from existing models, you can create a new model using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

**Parent Topic:**[Legacy Software Asset Management plugin](c_SoftwareAssetManagement.md)

**Related topics**  


[Legacy Software Asset Management plugin Overview module](c_SWAssetMgmtOverviewMod.md)

[Legacy Software Asset Management plugin setup process](c_SetupProcess.md)

[Determine where software is installed using the legacy Software Asset Management plugin](c_DeterminWhereSWInstalled.md)

[Software licenses in the legacy Software Asset Management plugin](c_SoftwareLicenses.md)

[Manage software models using the legacy Software Asset Management plugin](../task/t_ManagingSoftwareModels.md)

[License calculations with the legacy Software Asset Management plugin](c_UseLicenseCalculations.md)

[Legacy Software License Compliance Checker](c_SoftwareLicenseComplianceChecker.md)

[Software license reconciliation counters for the legacy Software Asset Management plugin](c_UseCountersSWLicenseReconcil.md)

[Legacy IBM PVU Process Pack](c_IBMPVUProcessPack.md)

[Software contracts for the legacy Software Asset Management plugin](c_SoftwareContracts.md)

[Legacy Oracle process pack](c_OracleProcessPack.md)

