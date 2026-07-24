---
title: Service Graph Connector for Tanium
description: Use the Service Graph Connector for Tanium to bring in hardware, software, and software usage data from a Tanium environment into your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/cmdb-integration-tanium.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Tanium

Use the Service Graph Connector for Tanium to bring in hardware, software, and software usage data from a Tanium environment into your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

<table id="table_yh4_wm1_mbc"><thead><tr><th>

Tanium

</th><th>

ServiceNow

</th></tr></thead><tbody><tr><td>

-   Tanium 1.9 or later versions for hardware and software
-   Tanium 1.17 or later versions for software usage

</td><td>

-   Washington DC
-   Xanadu
-   Yokohama

</td></tr></tbody>
</table>## Important information for upgrading Service Graph Connector for Tanium

Tanium Platform 7.6.2 or later versions support token-based authorization only. After you have installed the latest version of the Service Graph Connector for Tanium, verify the following configurations to use Tanium Platform 7.6.2 or later versions in your on-premise setups:

-   For a single instance, reconfigure the authentication type of an existing connection to use token-based authorization.
-   For multiple instances, deactivate the existing scheduled jobs for previously configured instances that used basic authorization, and then create and configure new instances to use token-based authorization.

## Configuring a connection

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Tanium using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgcc-configure-tanium.md).

**Important:** Unless there are configuration issues, use SGC Central to configure the connection. The guided setup method for configuration is being deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Tanium integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

## Data mapping

Data from the Tanium data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The following table describes the data sources, the staging tables, and the target tables including CMDB CI and non-CMDB CI classes for the Tanium application.

<table id="table_udz_pgq_1bc" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th><th>

Resource types

</th></tr></thead><tbody><tr><td>

SG-Tanium Applications

</td><td>

SG-Tanium Applications \[sn\_tanium\_integ\_sg\_tanium\_applications\]

</td><td>

[Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-tanium-classes.md)

 Running Process

 TCP

</td><td>

Applications

</td></tr><tr><td>

SG-Tanium Hardware and Software

</td><td>

SG Tanium Import \[sn\_tanium\_integ\_sg\_tanium\_import\]

</td><td>

[Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-tanium-classes.md)

 [File System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-tanium-classes.md)

 [Disk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-tanium-classes.md)

 [IP Address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-tanium-classes.md)

 When the Software Asset Management \(SAM\) application isn't installed:

 [Software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-tanium-classes.md)

 [Software Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-tanium-classes.md)

 When the SAM application is installed:

 [Software Installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-tanium-classes.md)

</td><td>

Server and software

</td></tr><tr><td>

SG-Tanium Usage

</td><td>

SG Tanium Usage Import \[sn\_tanium\_integ\_sg\_tanium\_usage\_import\]

</td><td>

Software Usage \[samp\_sw\_usage\]

</td><td>

None

</td></tr><tr><td>

SG-Tanium Remove Software

</td><td>

Integration Commons Remove Record \[sn\_cmdb\_int\_util\_remove\_record\]

</td><td>

None

</td><td>

None

</td></tr></tbody>
</table>**Note:**

-   The SG-Tanium Usage data source is available only when the Software Asset Management Professional plugin \(com.snc.samp\) plugin is activated on your ServiceNow instance. See [Request Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/t_RequSoftwareAssetMgmt.md).
-   The SG-Tanium Remove Software data source creates import sets and uses the transform map-based method for removing any target records for software data that weren't updated in the last delta query check. See [Managing CMDB data deletion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/cmdb-integ-record-removal.md).
-   Starting with the Service Graph Connector for Tanium 1.8.0 release, a buffer time is added for software removal when the **buffer\_days\_from\_last\_scan\_for\_hardware** system property is enabled. When this system property is enabled, the software removal candidate is removed only if the last scan time of the hardware on which the software removal candidate is installed is earlier than the last success import time + buffer time. To enable this property, set the value of the **buffer\_days\_from\_last\_scan\_for\_hardware** system property to a non-zero numeral value according to the number of days of buffer that you require. To disable this property, set the value to `0`.

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

## Additional resource

[How do I configure the Tanium Service Graph Connector?](https://www.servicenow.com/community/cmdb-articles/tanium-service-graph-connector/ta-p/2754467) article on the ServiceNow Community site

**Related topics**  


[Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md)

