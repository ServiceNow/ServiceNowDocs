---
title: Engineering license management
description: Get visibility into your license position and usage of your engineering applications to eliminate audit risks, inefficient usage of licenses, inaccurate forecasting, and to help prevent denials.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Engineering license management

Get visibility into your license position and usage of your engineering applications to eliminate audit risks, inefficient usage of licenses, inaccurate forecasting, and to help prevent denials.

Watch this short video for an introduction to engineering license management.

Overview of Engineering license management 

**Note:** To access all the benefits of the Software Asset Management Professional for engineering applications, request the Software Asset Management Professional for Engineering Applications plugin \(com.sn\_samp\_eng\_app\). For more information, see [Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md).

Engineering applications refer to categorizing software products in industries such as aerospace, oil and gas, and construction.

A concurrent license enables multiple users to share access to software applications from any computer on a network or from a virtual machine. License management servers that are installed on the network manage the distribution of a pool of shared licenses.

You can have multiple license management servers; one for each engineering application. The number of concurrent licenses in the shared pool determines the number of users who can use the software application at a given time. When you want to use an application, that application sends a request to the appropriate license management server to determine if a license is available. If a license is available, the application starts and the number of available licenses decreases by one. When the user exits the application, the license returns to the pool.

The following graphic illustrates the way OpenLM and Open iT work with the ServiceNow instance.

![Engineering License Manager](../image/optimize-engnrg-software-licenses.png)

The Software Asset Management application supports three types of licenses: floating, network, and token licenses. For information on these licenses, see [Software license metrics](c_SAMLicenseMetrics.md).

The ServiceNow instance integrates with OpenLM and Open iT to collect data from license management servers. OpenLM and Open iT are software license monitoring and management tools that integrate with a wide variety of license management servers such as IBM License Use Management \(LUM\), Sentinel Technologies, and Bentley Systems, Inc. Both OpenLM and Open iT connect with each license management server, consolidate the data, and get the data into your ServiceNow instance via the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) application.

After you download the ServiceNow Store application and configure the application via Guided Setup, both OpenLM and Open iT trigger data collection from all the license management servers that are connected to either of these. Data such as license usage, denials, user activity, and alerts are collected from the license management servers by OpenLM and Open iT, and transferred to the ServiceNow instance. The data is normalized and reconciled to produce reports. You can see the total spend on engineering software, the most denied products, license usage over time, and many other reports on the [Engineering License Overview dashboard](engineering-overview-dashboard.md) \(Software Asset Management classic application\) or the [Engineering License overview dashboard in workspace](../reference/engineering-license-dashboard-workspace.md) \(Software Asset Workspace\).

**Important:** For more details on the OpenLM setup and configuration, refer to the Supporting Links and Docs section of the [OpenLM Adapter Integration](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9eb1cd69db66fb007c1c40ceaa9619bc/1.3.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DOpenLM&sl=sh) page in the ServiceNow Store.

For more details on the Open iT setup and configuration, refer to the [Open iT LicenseAnalyzer](https://store.servicenow.com/sn_appstore_store.do#!/store/application/e127795897403110d365fca6f053af97/1.0.8)page in the ServiceNow Store.

**Parent Topic:**[Supported software publisher licenses](sam-publisher-packs.md)

