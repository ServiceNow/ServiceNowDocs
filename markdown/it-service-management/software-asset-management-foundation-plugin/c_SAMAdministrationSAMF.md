---
title: Software Asset Management Foundation plugin Administration
description: Software Asset Management Foundation plugin administration tasks include adding custom product records, creating custom license metrics, and setting properties. You can also refresh processor definitions, and migrate software installations.
locale: en-US
release: australia
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software Asset Management Foundation plugin Administration

Software Asset Management Foundation plugin administration tasks include adding custom product records, creating custom license metrics, and setting properties. You can also refresh processor definitions, and migrate software installations.

The sam\_admin role is required to configure administrative tasks. However, the sam\_user role can view and read configurations.

-   **[Add a Software Asset Management Foundation plugin custom software product](../task/t_AddACustomProductSAMF.md)**  
You can add a custom product if a software product does not exist in the Software Library. Custom products enable you to normalize and account for homegrown software, or software that is not yet part of the Software Library.
-   **[Add a Software Asset Management Foundation plugin custom license metric](../task/add-custom-license-metric-samf.md)**  
You can add a custom license metric to modify the default reconciliation process.
-   **[Migrate Software Asset Management Foundation plugin software installations](../task/t_MigrateSWInstallsSAMF.md)**  
If you are using Discovery, run this script after installing Software Asset Management Foundation plugin to copy previously discovered software installation records from the \[cmdb\_software\_instance\] table to the \[cmdb\_sam\_sw\_install\] table, which is used by Software Asset Management Foundation plugin to store software installation records.
-   **[Software Asset Management Foundation plugin properties](../reference/sam-properties-samf.md)**  
You can set default reconciliation properties such as reconciliation run with custom license metrics, and reconciliation debugging settings.
-   **[Software Asset Management Foundation plugin migration](c_SAMMigrationSAMF.md)**  
Migrate from the Software Asset Management plugin to the Software Asset Management Foundation plugin to take advantage of more powerful features. Manual actions by the customer are required after plugin activation.

**Parent Topic:**[Software Asset Management Foundation plugin](c_SoftwareAssetMgmtSAMF.md)

