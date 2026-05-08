---
title: Service Graph Connector for Microsoft Intune
description: Use the Service Graph Connector for Microsoft Intune to pull data from the Microsoft Intune application into your ServiceNow instance.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Microsoft Intune

Use the Service Graph Connector for Microsoft Intune to pull data from the Microsoft Intune application into your ServiceNow instance.

The Service Graph Connector for Microsoft Intune pulls data from mobile devices, computers and software applications into the ServiceNow® Configuration Management Database \(CMDB\) application. The integration provides greater visibility into mobile devices, computers and related software applications that run on them.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

<table id="table_bc2_11z_lbc"><thead><tr><th>

Microsoft Intune

</th><th>

ServiceNow

</th></tr></thead><tbody><tr><td>

-   Microsoft Intune Graph API v1.0
-   Microsoft Intune Graph API Beta

</td><td>

-   Yokohama
-   Zurich
-   Australia

</td></tr></tbody>
</table>## Use cases

The following are examples on how you can use the Service Graph Connector for different ServiceNow® applications:

-   IT Operations Management \(ITOM\) Visibility
    -   Detailed hardware and application inventory for Android, Apple, and Windows mobile devices. The inventory can be used with or without Software Asset Management \(SAM\).
    -   Compliance tracking for mobile devices. You can build your own device \(BYOD\) or use corporate-owned devices.
-   IT Service Management \(ITSM\)
    -   Incidents, problems, and changes on discovered configuration items \(CI\).
    -   Ownership tracking and assignment for mobile devices.

You can also do the following types of administrative actions:

-   Device Management: You can report on various aspects of the device.
-   Integration with Azure Monitor: Delta notification.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for Microsoft Intune using SGC Central](../../sgc-central/task/sgcc-configure-intune-integ.md).

**Important:** The guided setup method is deprecated from version 2.7.0 of the Service Graph Connector for Microsoft Intune. Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector.

## CMDB integration dashboards

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Microsoft Intune integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from data sources in the Microsoft Intune application is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The following table describes the data sources, the staging tables, and the target tables as CMDB CI classes, and the resource types imported for a Microsoft Intune application.

<table id="table_udz_pgq_1bc" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

CMDB CI classes

</th><th>

Resource types

</th><th>

Data source type

</th></tr></thead><tbody><tr><td>

SG-Intune Computer

</td><td>

SG-Intune Computer \[sn\_intune\_integrat\_computer\]

</td><td>

[Computer](../reference/cmdb-intune-classes.md#section_z3h_sr3_k5b)

 [SG-Intune Computer Related](../reference/cmdb-intune-classes.md#section_fbc_hdv_lbc)

 [IP Address](../reference/cmdb-intune-classes.md#section_it4_fdv_lbc)

 [Serial Number](../reference/cmdb-intune-classes.md#section_uyh_gdv_lbc)

 When the Software Asset Management \(SAM\) application isn't installed:

 [Software](../reference/cmdb-intune-classes.md#section_fw5_3dv_lbc)

 [Software Instance](../reference/cmdb-intune-classes.md#section_l4k_jdv_lbc)

 When the SAM application is installed: [Software Installation](../reference/cmdb-intune-classes.md#section_cgz_ddv_lbc)

</td><td>

Computers

</td><td>

Regular

</td></tr><tr><td>

SG-Intune Devices

</td><td>

SG-Intune Devices \[sn\_intune\_integrat\_devices\]

</td><td>

[Handheld Computing Device](../reference/cmdb-intune-classes.md#section_wsz_cdv_lbc)

 [Serial Number](../reference/cmdb-intune-classes.md#section_uyh_gdv_lbc)

 [Network Adapter](../reference/cmdb-intune-classes.md#section_abw_2dv_lbc)

 [SG-Intune Device Related](../reference/cmdb-intune-classes.md#section_pwb_3dv_lbc)

 [IP Address](../reference/cmdb-intune-classes.md#section_it4_fdv_lbc)

 When the Software Asset Management \(SAM\) application isn't installed:

 [Software](../reference/cmdb-intune-classes.md#section_fw5_3dv_lbc)

 [Software Instance](../reference/cmdb-intune-classes.md#section_l4k_jdv_lbc)

 When the SAM application is installed: [Software Installation](../reference/cmdb-intune-classes.md#section_cgz_ddv_lbc)

</td><td>

Mobile devices

</td><td>

Regular

</td></tr><tr><td>

SG-Intune Software

</td><td>

SG-Intune Software \[sn\_intune\_integrat\_software\]

</td><td>

[Software](../reference/cmdb-intune-classes.md#section_fw5_3dv_lbc)

</td><td>

Discovered apps

</td><td>

Regular

</td></tr><tr><td>

SG-Intune Device Reports

</td><td>

SG-Intune Device Reports \[sn\_intune\_integrat\_device\_reports\]

</td><td>

[Computer](../reference/cmdb-intune-classes.md#section_z3h_sr3_k5b) or [Handheld Computing Device](../reference/cmdb-intune-classes.md#section_wsz_cdv_lbc)

 [Serial Number](../reference/cmdb-intune-classes.md#section_uyh_gdv_lbc)

 [Network adapter](../reference/cmdb-intune-classes.md#section_abw_2dv_lbc)

 [SG-Intune Computer Related](../reference/cmdb-intune-classes.md#section_fbc_hdv_lbc)

 [SG-Intune Device Related](../reference/cmdb-intune-classes.md#section_pwb_3dv_lbc)

 [IP Address](../reference/cmdb-intune-classes.md#section_it4_fdv_lbc)

**Note:** Imports Wireless \(Wi-Fi\) IPv4 Address of a device only.

 When the Software Asset Management \(SAM\) application isn't installed:

 [Software](../reference/cmdb-intune-classes.md#section_fw5_3dv_lbc)

 [Software Instance](../reference/cmdb-intune-classes.md#section_l4k_jdv_lbc)

 When the SAM application is installed: [Software Installation](../reference/cmdb-intune-classes.md#section_cgz_ddv_lbc)

</td><td>

Computers and mobile devices

</td><td>

Advanced

</td></tr><tr><td>

SG-Intune Software Reports

</td><td>

SG-Intune Software Reports \[sn\_intune\_integrat\_software\_reports\]

</td><td>

When the Software Asset Management \(SAM\) application isn't installed:

 [Software](../reference/cmdb-intune-classes.md#section_fw5_3dv_lbc)

 [Software Instance](../reference/cmdb-intune-classes.md#section_l4k_jdv_lbc)

 When the SAM application is installed: [Software Installation](../reference/cmdb-intune-classes.md#section_cgz_ddv_lbc)

</td><td>

Discovered apps

</td><td>

Advanced

</td></tr></tbody>
</table>Starting with the Service Graph Connector for Microsoft Intune 2.7.0 version, the SG-Intune Device Reports and SG-Intune Software Reports advanced data sources are not available by default. To use these advanced data sources, you must select the **Advanced data sources** option while configuring the connection using SGC Central. See [Configure Service Graph Connector for Microsoft Intune using SGC Central](../../sgc-central/task/sgcc-configure-intune-integ.md).

Configure the SG-Intune Device Reports and SG-Intune Software Reports advanced data sources for faster data import, better performance, and inclusion of software publisher details. Compared to the regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\), the advanced data sources help resolve server errors and performance issues caused by having a large number of Microsoft Intune devices.

For more information, see [Service Graph Connector For Microsoft Intune - Advanced \(Configure advanced Data sources\) \[KB1641546\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1641546).

**Note:** The SG-Intune Device Reports advanced data source is an alternative to the SG-Intune Computer and SG-Intune Devices regular data sources. The SG-Intune Software Reports advanced data source is an alternative to the SG-Intune Software data source. The data imported by the advanced data sources is similar to the data imported by the corresponding regular data sources.

After you complete setting up the connection, you can configure the integration to periodically pull data from the Microsoft Intune application.

**Note:**

-   For any discovered software applications that were deleted later in the Microsoft Intune application, the Service Graph Connector automatically deletes the corresponding records in CMDB.
-   To view more details about a handheld computing device or computer in the Computer \[cmdb\_ci\_computer\] class, enable the related lists SG-Intune Device Related and SG-Intune Computer Related.

    You can add these related lists by configuring the Related Lists view on the form that opens when you select a handheld computing device or computer configuration item \(CI\) in the Computer \[cmdb\_ci\_computer\] class. Computer CIs are displayed in the Computers list, accessed by navigating to **All** &gt; **Configuration** &gt; **Base Items** &gt; **Computers**. For more information about adding related lists to a form, see Configuring the form layout.


For more information on where data is saved when pulling data from a Microsoft Intune application, see [CMDB classes targeted in Service Graph Connector for Microsoft Intune](../reference/cmdb-intune-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Additional resources

-   [Service Graph Connector for Microsoft Intune - Troubleshooting connection issues](https://community.servicenow.com/community?id=community_blog&sys_id=a405ef9bdbbd7018bb4a474d13961903) article on the ServiceNow Community site
-   [Service Graph Connector For Microsoft Intune - Advanced \(Configure advanced Data sources\) \[KB1641546 \]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1641546) article in the Now Support Knowledge Base

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

[Configure Service Graph Connector for Microsoft Intune using SGC Central](../../sgc-central/task/sgcc-configure-intune-integ.md)

