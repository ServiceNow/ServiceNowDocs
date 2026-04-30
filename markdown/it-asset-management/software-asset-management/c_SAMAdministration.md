---
title: Software Asset Management administration
description: Software Asset Management administration tasks include adding custom part number records and custom license metrics. You can also refresh processor definitions and migrate software installations. Software Asset Management content service can be enabled, and migration procedures are also included.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Software Asset Management, IT Asset Management]
---

# Software Asset Management administration

Software Asset Management administration tasks include adding custom part number records and custom license metrics. You can also refresh processor definitions and migrate software installations. Software Asset Management content service can be enabled, and migration procedures are also included.

The sam\_admin role is required to configure administrative tasks. However, the sam\_user role can view and read configurations.

Software Asset Management job results show the status of discovery model normalization and software usage import jobs.

Software Asset Job Results records are listed in the navigation path **All** &gt; **Software Asset** &gt; **Administration** &gt; **Job Results** \(see table for field descriptions\).

|Field|Description|
|-----|-----------|
|Number|Number of the job result that is generated when the job is run.|
|Name|Name of the job.|
|Status|Status of the job.|
|Created|Date and time job was created.|
|Updated|Date and time job was updated.|

-   **[Enable sharing information with Software Asset Management content service](../task/t_EnableSAMContentService.md)**  
Opt in to share unnormalized software installation data from your organization with Software Asset Management Content Service. You can opt out at any time.
-   **[Exclude software assets on CIs](../task/exclude-software-assets-cis.md)**  
You may want to manage software assets installed on a subset of your configuration items in the Software Asset Management application.
-   **[Engineering license servers](eng-license-server.md)**  
View the list of all the license management servers that OpenLM or Open iT connect with to get data into your ServiceNow instance.
-   **[Add a software pattern normalization rule](../task/t_AddAPatternNormRule.md)**  
You can add a pattern normalization rule to normalize specific software products in your environment based on a common pattern.
-   **[Add a software reclamation rule](../task/t_AddAReclamationRule.md)**  
Add a reclamation rule to aggregate usage records and to identify unused software.
-   **[Create a custom file rule to manually define file sets](../task/create-custom-file-rule.md)**  
Create custom rules to manually define file sets and normalize data not recognized by the SAM API. After you have created custom rules, custom file sets can be discovered with File Signature Normalization and software records can be generated.
-   **[Configure third-party discovery sources for Software Asset Management](../task/configure-third-party-discovery.md)**  
Set up a third-party discovery source for Software Asset Management to populate the Software Installation \[cmdb\_sam\_sw\_install\] table with software found in your environment.
-   **[Delete uninstalled software from the Software Installation table](../task/delete-disco-entries-sam.md)**  
Delete installations from the Software Installation \[cmdb\_sam\_sw\_install\] table if those software installations are also uninstalled from a CI.
-   **[Create a reclamation rule to import Microsoft SCCM usage data](../task/create-reclamation-rule-sccm.md)**  
To import your Microsoft SCCM data, create a reclamation rule for the product that you want the usage information for.
-   **[Add a custom part number](../task/sam-add-custom-part-number.md)**  
You can add a custom part number to resolve an entitlement import error that occurs when a part number does not exist in the Software Library.
-   **[Add a custom license metric](../task/add-custom-license-metric.md)**  
You can add a custom license metric to modify the default reconciliation process.
-   **[Refresh processor definitions](../task/t_RefreshProcessorDef.md)**  
After activating Software Asset Management, refresh processor definitions to normalize processors on servers in the CMDB.
-   **[Migrate software installations](../task/t_MigrateSWInstalls.md)**  
If you are using Discovery, run this script after installing the Software Asset Management application to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by the Software Asset Management application to store software installation records.
-   **[Revert Software Asset Management customizations](../task/revert-sam-customizations.md)**  
After installing the Software Asset Management application for the first time, or upgrading from the Software Asset Management Foundation plugin, you need to revert customizations for all features work. The Revert Customizations module in the Software Asset Management application can revert customized files related to Software Asset Management back to the base configurations that were skipped during the installation or upgrade process.
-   **[Manage Software Library](../task/manage-sam-software-library.md)**  
Use the Manage Software Library module to manually upload software library data to on-premise instances \(instances not in the cloud to receive automatic Software Library updates\). You can also choose to export your normalization content for participation in the Software Asset Management content service.

**Parent Topic:**[Software Asset Management](c_SoftwareAssetMgmt.md)

