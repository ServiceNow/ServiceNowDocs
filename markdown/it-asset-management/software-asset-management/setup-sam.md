---
title: Setting up Software Asset Management
description: Before you can begin using the Software Asset Management application, complete the setup process.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software Asset Management, IT Asset Management]
---

# Setting up Software Asset Management

Before you can begin using the Software Asset Management application, complete the setup process.

You will need to request the Software Asset Management plugin. Then, integrate your discovery software so your software installation data can be pulled into your instance. You can then opt-in to the Software Asset Management Content Service Library to securely send your data back to ServiceNow. The data is used to help build the content service to automatically normalize your data. If necessary, determine if you need to exclude any software assets on configuration items that you manage.

-   **[Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md)**  
 The ServiceNow® Software Asset Management Professional \(com.snc.samp\) plugin requires a separate subscription. This plugin includes demo data. Depending on your environment, you may choose to request one or more related plugins.
-   **[Software Asset Management migration](c_SAMMigration.md#)**  
Migrate from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application to take advantage of more powerful features. Manual actions by the customer are required after plugin activation.
-   **[Configure SCCM for Software Asset Management](../task/configure-sccm-sam.md)**  
Set up Microsoft SCCM for Software Asset Management to populate the Software Installation \[cmdb\_sam\_sw\_install\] table with client software found in your environment. You can also set up SCCM for Client Software Distribution to reclaim unused and underused software.
-   **[Managing software suites](Manage-software-suites.md)**  
Simplify licensing and lower the cost of licenses from vendors. Get visibility into your complex suite licenses, manage compliance, and optimize your spending on these licenses.
-   **[Windows Server cluster license optimization](windows-cluster-optimization.md)**  
Optimize rights used for Windows Server clustering based on costs and compliance criteria.
-   **[Create a catalog request to reclaim assets](../task/create-catalog-req-offboardingsam.md)**  
Create a catalog request to efficiently reclaim software assets when an employee leaves an organization or moves to a different role.

**Parent Topic:**[Software Asset Management](c_SoftwareAssetMgmt.md)

