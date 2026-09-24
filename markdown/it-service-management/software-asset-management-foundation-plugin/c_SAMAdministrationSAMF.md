---
title: Basic Software Asset Management Administration
description: Basic Software Asset Management administration tasks include adding custom product records, creating custom license metrics, and setting properties. You can also refresh processor definitions, and migrate software installations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/software-asset-management-foundation-plugin/c\_SAMAdministrationSAMF.html
release: brazil
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Basic Software Asset Management, ITSM Software Asset Management, Asset Management common applications, IT Service Management]
---

# Basic Software Asset Management Administration

Basic Software Asset Management administration tasks include adding custom product records, creating custom license metrics, and setting properties. You can also refresh processor definitions, and migrate software installations.

The sam\_admin role is required to configure administrative tasks. However, the sam\_user role can view and read configurations.

-   **[Add a Basic Software Asset Management custom software product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/software-asset-management-foundation-plugin/t_AddACustomProductSAMF.md)**  
You can add a custom product if a software product does not exist in the Software Library. Custom products enable you to normalize and account for homegrown software, or software that is not yet part of the Software Library.
-   **[Add a Basic Software Asset Management custom license metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/software-asset-management-foundation-plugin/add-custom-license-metric-samf.md)**  
You can add a custom license metric to modify the default reconciliation process.
-   **[Migrate Basic Software Asset Management software installations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/software-asset-management-foundation-plugin/t_MigrateSWInstallsSAMF.md)**  
If you are using Discovery, run this script after installing Basic Software Asset Management to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by Basic Software Asset Management to store software installation records.
-   **[Basic Software Asset Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/software-asset-management-foundation-plugin/sam-properties-samf.md)**  
You can set default reconciliation properties such as reconciliation run with custom license metrics, and reconciliation debugging settings.
-   **[Basic Software Asset Management migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/software-asset-management-foundation-plugin/c_SAMMigrationSAMF.md)**  
Migrate from the Software Asset Management plugin to the Basic Software Asset Management to take advantage of more powerful features. Manual actions by the customer are required after plugin activation.

**Parent Topic:**[Basic Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/software-asset-management-foundation-plugin/c_SoftwareAssetMgmtSAMF.md)

