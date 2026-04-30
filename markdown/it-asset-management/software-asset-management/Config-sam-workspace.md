---
title: Configuring Software Asset Management
description: Configure the various aspects of the Software Asset Management application based on the needs of your organization.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software Asset Management, IT Asset Management]
---

# Configuring Software Asset Management

Configure the various aspects of the Software Asset Management application based on the needs of your organization.

## Configuration overview

Configuring the Software Asset Management application by the system administrators involves performing the following tasks. Depending on your organization's needs and requirements, some configuration tasks are optional.

|Task| |Resource|
|----|---|--------|
|Request the Software Asset Management application|Required|[Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md)|
|Overwrite customizations for Software Asset Management migration|Optional|[Overwrite customizations for Software Asset Management migration](../task/t_MigrateSAMCustom.md)|
|Configure SCCM for Software Asset Management.|Optional|[Configure SCCM for Software Asset Management](../task/configure-sccm-sam.md)|

-   **[Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md)**  
 The ServiceNow® Software Asset Management Professional \(com.snc.samp\) plugin requires a separate subscription. This plugin includes demo data. Depending on your environment, you may choose to request one or more related plugins.
-   **[Overwrite customizations for Software Asset Management migration](../task/t_MigrateSAMCustom.md)**  
When migrating from the Software Asset Management plugin \(ITSM Software Asset Management feature of Asset Management\) to the Software Asset Management application, further actions are required by the customer after plugin activation to ensure successful migration of customized forms and lists.
-   **[Configure SCCM for Software Asset Management](../task/configure-sccm-sam.md)**  
Set up Microsoft SCCM for Software Asset Management to populate the Software Installation \[cmdb\_sam\_sw\_install\] table with client software found in your environment. You can also set up SCCM for Client Software Distribution to reclaim unused and underused software.

**Parent Topic:**[Software Asset Management](c_SoftwareAssetMgmt.md)

