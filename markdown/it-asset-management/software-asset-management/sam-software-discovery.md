---
title: Software discovery
description: After you've imported your entitlements, use ServiceNow Discovery or Microsoft SCCM to discover software installations in your environment and transfer that data into the ServiceNow AI Platform.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software discovery and normalization, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software discovery

After you've imported your entitlements, use ServiceNow Discovery or Microsoft SCCM to discover software installations in your environment and transfer that data into the ServiceNow AI Platform.

![This graphic provides an overview of how to setup either ServiceNow Discovery or Microsoft SCCM.](../image/mmasset0021825software-discovery-and-normalization.svg "Infographic showing setting up of ServiceNow Discovery or Microsoft SCCM")

While you may use Discovery Home for datacenters and Microsoft SCCM for desktop environments, you can integrate other third-party discovery solutions with CMDB to support Software Asset Management. To integrate a different discovery solution, add it manually, or you can download an application, from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For more information about integrating a discovery source manually, see the [Customer Success Center](https://www.servicenow.com/success.html).

To learn more about collecting data after you've integrated with both Discovery and SCCM, see Collect software data with either SCCM or Discovery.

## Discovery integration

ServiceNow Discovery is used to automatically populate the Software Installations table so the software can be normalized and reconciled.

**Note:** To use Discovery, the Discovery plugin must be activated.

Discovery uses patterns in the discovery process that can be created or customized. The base system contains a wide range of patterns that cover most industry standard network devices and applications. The following are some of the base system patterns used by Software Asset Management.

-   Citrix XenApp
-   Citrix XenDesktop,
-   VMware vCenter
-   Microsoft SQL Server
-   Microsoft Exchange Server
-   Oracle Database Server

You can also customize other patterns for Software Asset Management. For more information, see Create or modify patterns.

Discovered software is stored in the Software Installations \[cmdb\_sam\_sw\_install\] table.

When software install records are written to the Software Installations table, a business rule verifies whether the unique combination of the discovered publisher, discovered product, and discovered version exist in the Discovery Model table.

-   If so, the reference to the discovery model is set in the Software Installations table.
-   If not, a new record is created in the Discovery Model table, and that discovery model reference is set in the Software Installations table.

After discovery, normalization is run.

For more information on Discovery, see Discovery with Software Asset Management.

## SCCM integration

You can use SCCM by itself or with Discovery Home to identify software on your devices.

**Note:** While you may use Microsoft SCCM for discovering software installations in your desktop environments, you can integrate other third-party tools.

Both Microsoft SCCM 2012 v2 and 2016 plugins are certified with Software Asset Management. The corresponding Microsoft SCCM Integration plugin must be installed to integrate Microsoft SCCM with Software Asset Management.

Microsoft SCCM Integration plugins:

-   Integration — Microsoft SCCM 2012 v2 \(com.snc.integration.sccm2012v2\) plugin
-   Integration — Microsoft SCCM 2016 \(com.snc.integration.sccm2016\) plugin

Microsoft SCCM Software Usage plugins:

-   Integration — Microsoft SCCM 2012 v2 Software Usage \(com.snc.samp\_usage\_sccm\) plugin
-   Integration — Microsoft SCCM 2016 Software Usage \(com.snc.samp.usage\_sccm\_2016\) plugin

The Integration — Microsoft SCCM 2016 plugin is compatible with SCCM versions 1606, 1906, 1910, and 2002.

**Important:** These Microsoft SCCM plugins will be deprecated in the Tokyo release. If you are integrating with SCCM for the first time, request and install the Service Graph connector for Microsoft SCCM application from the [ServiceNow Store](https://store.servicenow.com/) instead. If you have already activated one of the Microsoft SCCM plugins on your ServiceNow instance, use the Migration Readiness Tool for Service Graph Connector for SCCM store application to prepare your instance for migration from the Microsoft SCCM plugin to the Service Graph connector. See Service Graph connector for Microsoft SCCM for more information on the Service Graph connector.

For more information on SCCM and how to import your data into your instance, see [Microsoft SCCM software usage](sccm-software-usage.md).

**Parent Topic:**[Software discovery and normalization](c_SAMDiscovery.md)

