---
title: Engineering license management
description: Monitor engineering licenses and usage through OpenLM and Open iT to eliminate audit risks, ensure license optimization, reduce inaccurate forecasting, and prevent denials. These license management services ensure accurate forecasting for software in industries such as aerospace, oil and gas, and construction.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Engineering license management

Monitor engineering licenses and usage through OpenLM and Open iT to eliminate audit risks, ensure license optimization, reduce inaccurate forecasting, and prevent denials. These license management services ensure accurate forecasting for software in industries such as aerospace, oil and gas, and construction.

Watch this short video for an introduction to engineering license management.

Overview of Engineering license management 

**Note:** To access the benefits of the Software Asset Management Professional for engineering applications, request the Software Asset Management Professional for Engineering Applications store app \(sn\_samp\_eng\_app\). For more information, see [Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md).

## Engineering license management overview

OpenLM and Open iT are software license monitoring and management tools that integrate with a wide variety of license management servers such as IBM License Use Management \(LUM\), Sentinel Technologies, Autodesk, Inc., and Bentley Systems, Inc. OpenLM and Open iT connect with each license management server, consolidate the data, and get the data into your ServiceNow instance via the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) application.

The following graphic illustrates how OpenLM and Open iT work with the ServiceNow instance.

After you download the ServiceNow Store application and configure the application via Guided Setup, OpenLM and Open iT trigger data collection from all the license management servers that are connected to either of these. Data such as license usage, denials, user activity, and alerts are collected from the license management servers, and transferred to the ServiceNow instance. The data is normalized and reconciled to produce reports. You can see the total spend on engineering software, the most denied products, license usage over time, and other reports on the [Engineering License Overview dashboard](engineering-overview-dashboard.md) \(Software Asset Management classic application\) or the [Engineering License overview dashboard in workspace](../reference/engineering-license-dashboard-workspace.md) \(Software Asset Workspace\).

**Important:** For more details on the OpenLM setup and configuration, refer to the Supporting Links and Docs section of the [OpenLM Adapter Integration](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9eb1cd69db66fb007c1c40ceaa9619bc/1.3.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DOpenLM&sl=sh) page in the ServiceNow Store.

For more details on the Open iT setup and configuration, refer to the [Open iT LicenseAnalyzer](https://store.servicenow.com/sn_appstore_store.do#!/store/application/e127795897403110d365fca6f053af97/1.0.8) page in the ServiceNow Store.

## Types of licenses supported for engineering applications

The Software Asset Management application supports various types of licenses for engineering applications.

-   **Concurrent licenses**

    A concurrent license enables multiple users to share access to software applications from any computer on a network or from a virtual machine. License management servers that are installed on the network manage the distribution of a pool of shared licenses. The types of concurrent licenses include floating, network, and token licenses.

    You can have multiple license management servers; one for each engineering application. The number of concurrent licenses in the shared pool determines the number of users who can use the software application at a given time. When you want to use an application, that application sends a request to the appropriate license management server to determine if a license is available. If a license is available, the application starts and the number of available licenses decreases by one. When the user exits the application, the license returns to the pool.

-   **Subscription licenses**

    A subscription license enables users to access software applications for a specified period. Each license is assigned to an individual user. The Software Asset Management application supports subscription licenses, such as the Autodesk named user subscription license, to ensure accurate usage tracking of engineering applications. The Autodesk named user subscription license uses identity-based user profiles accessing cloud-based licenses.

-   **Resource consumption**

    A resource consumption-based license metric supports client access license \(CAL\) reconciliation. This license metric represents a 1:1 ratio calculation between the Unit consumption column in the Resource Value \[samp\_sw\_resource\_value\] table and the Licenses required column in the License Metric Results \[samp\_license\_metric\_result\] table. The Software Asset Management application supports consumption-based licenses for license management servers such as Bentley Systems, Inc.


For more information on license metrics and metric groups, see [Software license metrics](c_SAMLicenseMetrics.md).

-   **[Tables installed with engineering applications](../reference/components-installed-engg-app.md)**  
Tables are installed with the Software Asset Management Professional for Engineering Applications store app \(sn\_samp\_eng\_app\).
-   **[Publisher overview for Bentley Systems in the Software Asset Workspace](../reference/publisher-overview-engg-app.md)**  
View license usage information for Bentley Systems and its software models in the publisher overview in the Software Asset Workspace.

**Parent Topic:**[Supported software publisher licenses](sam-publisher-packs.md)

