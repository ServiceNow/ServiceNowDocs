---
title: Service Graph Connector for Microsoft SCCM
description: Use the Service Graph Connector for Microsoft SCCM to pull data from Microsoft System Center Configuration Manager \(SCCM\) into your ServiceNow instance.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-09-07"
reading_time_minutes: 5
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Microsoft SCCM

Use the Service Graph Connector for Microsoft SCCM to pull data from Microsoft System Center Configuration Manager \(SCCM\) into your ServiceNow instance.

The Service Graph Connector for Microsoft SCCM \(SG-SCCM\) imports SCCM data into the ServiceNow® Configuration Management Database \(CMDB\) application. The integration does not write to the SCCM database and supports the Microsoft Endpoint Configuration Manager \(MECM\). The integration pulls data from computers, processors, operating systems, disks, networks, and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Supported Microsoft SCCM/MECM versions:
    -   2503
    -   2409
-   Supported ServiceNow versions:
    -   Xanadu
    -   Yokohama
    -   Zurich

## Use cases

The following ServiceNow applications have features that interact with the Service Graph Connector:

-   [IT Operations Management \(ITOM\) Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
    -   Ability to get visibility into your infrastructure.
    -   Detailed hardware and software inventory tracking. The tracking can be done with or without Software Asset Management \(SAM\).
    -   Ability to detect delta changes for efficient incremental imports from SCCM to the ServiceNow AI Platform.
-   [IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
    -   Incidents, problems, and changes on discovered configuration items \(CI\).
    -   Automatic device ownership assignment.
-   [Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) and [IT Asset Management \(ITAM\)](https://www.servicenow.com/docs/access?context=it-asset-management&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
    -   Tight integration with Software Asset Management Professional and client software distribution workflows.
    -   Inventory Software package and installation tracking.
    -   Software Usage tracking.
    -   License reclamation by detecting removed software.
    -   Support for software editions, normalizing publisher information, and normalizing product Information.
    -   Support for SCCM Asset Intelligence.

## Important information for upgrading Service Graph Connector for Microsoft SCCM

After you've installed the latest version of the Service Graph Connector for Microsoft SCCM, ensure that you have removed the **last\_run\_datetime** field value from the Data Source \[sys\_data\_source\] table for the SCCM data sources.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for Microsoft SCCM using SGC Central](../../sgc-central/task/sgcc-configure-sccm-integ.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Microsoft SCCM integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the SCCM data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow® CMDB using the Identification and Reconciliation Engine \(IRE\).

The SCCM data sources include the following:

-   SG-SCCM Computer Identity

    You can see the following data if it is available in SCCM:

    -   Asset Tag. If the Asset Tag data is available, the mapping can be optionally enabled via the guided setup.
    -   Assigned
    -   DNS Domain
-   SG-SCCM Computer OU. This data source imports data about the Organizational Unit \(OU\) name. The data is stored in the SG-SCCM Computer Related \[sn\_sccm\_integrate\_sccm\_2019\_computer\_related\] table. To add the view, open the computer record, click the top header, and select **View** &gt; **SG-SCCM Computer Related**.
-   SG-SCCM Disk
-   SG-SCCM Last Discovered Update. This data source will run at the end of the import schedules to update the last\_discovered date on the Computer CI. The source will conduct a full pull of all the computers and bring in only the ResourceID and the LastHWScan columns to update the CMDB Computer table.
-   SG-SCCM Network
-   SG-SCCM Operating System
-   SG-SCCM Processor
-   SG-SCCM Removed Software. Ensure the **Use last run datetime** option is cleared for every run.
-   SG-SCCM Removed Software AI. Ensure the **Use last run datetime** option is cleared for every run.
-   SG-SCCM Software
-   SG-SCCM Software AI

**Note:** If you have Asset Intelligence on your Microsoft SCCM instance, you have to run SG-SCCM Removed Software AI and SG-SCCM Software AI. If you do not have Asset Intelligence on your instance, you have to run SG-SCCM Removed Software and SG-SCCM Software.

When you complete setting up the connection, you can configure the integration to periodically pull data from SCCM. The data is loaded into staging tables and then inserted into the following target tables:

-   CI Relationship \[cmdb\_rel\_ci\]
-   Computer \[cmdb\_ci\_computer\] \(required\)
-   Disk \[cmdb\_ci\_disk\]
-   IP address \[cmdb\_ci\_ip\_address\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Serial Number \[cmdb\_serial\_number\]
-   Software Installation \[cmdb\_sam\_sw\_install\] \(If the SAM application is installed.\)
-   Software Instance \[cmdb\_software\_instance\] \(If the SAM application is not installed.\)
-   Software \[cmdb\_ci\_spkg\] \(If the SAM application is not installed.\)
-   Software Usage \[samp\_sw\_usage\]

For more information on where data is saved when pulling data from a Microsoft SCCM application, see [CMDB classes targeted in Service Graph Connector for Microsoft SCCM](../reference/cmdb-sccm-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Resolving the missing IP address or MAC address issue

By default, network adapters that are missing an IP address or MAC address are not imported. To include these network adapters in the import, do the following:

1.  Navigate to **Service Graph Connector for Microsoft SCCM** &gt; **Data Sources**.
2.  Select **SG-SCCM Network**.
3.  Remove the where clause from the **SQL statement** field.

## Additional resources

-   [How do I configure the SG-SCCM Service Graph Connector?](https://www.servicenow.com/community/cmdb-articles/sg-sccm-service-graph-connector/ta-p/2854458) article on the ServiceNow Community site
-   [Service Graph Connector for Microsoft SCCM - FAQ and Troubleshooting](https://community.servicenow.com/community?id=community_blog&sys_id=a753807adb7eb0d0fd8d2b69139619a8) blog post on the ServiceNow Community site
-   [Service Graph Connector for Microsoft SCCM 3.0 Setup Guidelines \[KB1001248\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1001248) article in the Now Support Knowledge Base
-   [Support for Removed Software functionality in Service Graph Connector for SCCM integration](https://www.servicenow.com/community/cmdb-blog/support-for-removed-software-functionality-in-service-graph/ba-p/2274937) blog post on the ServiceNow Community site

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

