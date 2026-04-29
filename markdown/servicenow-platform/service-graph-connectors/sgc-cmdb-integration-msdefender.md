---
title: Service Graph Connector for Microsoft Defender Endpoint
description: Use the Service Graph Connector for Microsoft Defender Endpoint to pull data from machines protected by the Microsoft Defender for Endpoint security solution into your ServiceNow instance.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Microsoft Defender Endpoint

Use the Service Graph Connector for Microsoft Defender Endpoint to pull data from machines protected by the Microsoft Defender for Endpoint security solution into your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Supported Microsoft Defender for Endpoint versions:
    -   Microsoft Defender for Endpoint Plan 1
    -   Microsoft Defender for Endpoint Plan 2
-   Supported ServiceNow versions:
    -   Washington DC
    -   Xanadu
    -   Yokohama

## Use cases

The ServiceNow Security Operations applications have features that interact with the Service Graph Connector to gain insights into machines utilizing the Microsoft Defender for Endpoint security solution.

## Important Information for upgrading Service Graph Connector for Microsoft Defender Endpoint

After you upgrade to Service Graph Connector for Microsoft Defender Endpoint 1.2.0, migrate data from the Server \[cmdb\_ci\_server\] CI class to the Computer \[cmdb\_ci\_computer\] CI class. For more information, see the [Service Graph Connector for Microsoft Defender Endpoint - Data migration after upgrade to version 1.2.0 \[KB2096769\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2096769) article in the Now Support Knowledge Base.

## Configuring a connection for the connector

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Microsoft Defender Endpoint using SGC Central](../../sgc-central/task/sgcc-configure-msdefender.md).

**Important:** Unless there are configuration issues, use SGC Central to configure the connection. The guided setup method for configuration is being deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Microsoft Defender for Endpoint integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Microsoft Defender for Endpoint data source is mapped and transformed into the ServiceNow CMDB configuration item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to pull data periodically from the machines utilizing the Microsoft Defender for Endpoint security solution.

The following data source is included for the Microsoft Defender for Endpoint security solution:

-   **SG-Defender Machines**

    Imports all the machine-related data from the machines utilizing the Microsoft Defender for Endpoint security solution, loads the imported data in the SG-Defender Machines \[sn\_defender\_integ\_sg\_defender\_machines\] staging table, and then populates the following target tables:

    -   IP Address \[cmdb\_ci\_ip\_address\]
    -   Software Installation \[cmdb\_sam\_sw\_install\] \(If the Software Asset Management \(SAM\) application is installed.\)
    -   Software Instance \[cmdb\_software\_instance\] \(If the SAM application is not installed.\)
    -   Software \[cmdb\_ci\_spkg\] \(If the SAM application is not installed.\)
    -   SG-Defender Machines Related \[sn\_defender\_integ\_sg\_defender\_machines\_related\]
    -   Network Adapter \[cmdb\_ci\_network\_adapter\]
    -   Computer \[cmdb\_ci\_computer\]
    -   Windows Server \[cmdb\_ci\_win\_server\]

**Note:** Only operating system details are populated in the Software Installation \[cmdb\_sam\_sw\_install\], Software Instance \[cmdb\_software\_instance\], and Software \[cmdb\_ci\_spkg\] tables.

For more information on where data is saved when pulling data from the Microsoft Defender for Endpoint security solution, see [CMDB classes targeted in Service Graph Connector for Microsoft Defender Endpoint](../reference/sgc-cmdb-msdefender-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

