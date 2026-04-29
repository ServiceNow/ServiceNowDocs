---
title: Service Graph Connector for SolarWinds
description: Use the Service Graph Connector for SolarWinds to pull in data from the SolarWinds software into your ServiceNow instance.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for SolarWinds

Use the Service Graph Connector for SolarWinds to pull in data from the SolarWinds software into your ServiceNow instance.

The Service Graph Connector for SolarWinds pulls in asset inventory data \(hardware and software\) from the SolarWinds database into the ServiceNow® Configuration Management Database \(CMDB\) application.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Supported SolarWinds Orion minimum versions:
    -   2019.4 HF6
    -   2020.2.1. HF2
-   Supported ServiceNow versions:
    -   Washington DC
    -   Xanadu
    -   Yokohama

## Use cases

The following are examples on how you can use the Service Graph Connector:

-   Automatic normalization of asset information for hardware, virtualization and cloud resources, and software.
-   Ability to configure and save synchronization schedules.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for SolarWinds using SGC Central](../../sgc-central/task/sgcc-configure-solarwinds-integ.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecation.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed Service Graph Connectors. You can see metrics for all integration runs. You can filter the view to a specific integration, a specific time duration, or a specific integration run. For more details about monitoring SolarWinds integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from data sources in the SolarWinds software is mapped and transformed into ServiceNow CMDB tables using the Robust Transform Engine \(RTE\). Data is inserted into ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from the SolarWinds software.

The data is loaded into staging tables and then inserted into the following CMDB target tables:

-   AIX Server \[cmdb\_ci\_aix\_server\]
-   Availability Zone \[cmdb\_ci\_availability\_zone\]
-   CI Relationship \[cmdb\_rel\_ci\]
-   Cloud Network \[cmdb\_ci\_network\]
-   Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]
-   Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]
-   Computer \[cmdb\_ci\_computer\]
-   Disk \[cmdb\_ci\_disk\]
-   Hardware \[cmdb\_ci\_hardware\]
-   Hardware Type \[cmdb\_ci\_compute\_template\]
-   Hyper-V Server \[cmdb\_ci\_hyper\_v\_server\]
-   IIS Virtual Directory \[cmdb\_ci\_iisdirectory\]
-   Image \[cmdb\_ci\_os\_template\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Linux Server \[cmdb\_ci\_linux\_server\]
-   Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]
-   Microsoft iis Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\]
-   MS SQL Server \[cmdb\_ci\_db\_mssql\_server\]
-   MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Network Gear \[cmdb\_ci\_netgear\]
-   Serial Number \[cmdb\_serial\_number\]
-   Server \[cmdb\_ci\_server\]
-   Software Installation \[cmdb\_sam\_sw\_install\] \(If the Software Asset Management \(SAM\) application is installed.\)
-   Software Instance \[cmdb\_software\_instance\] \(If the SAM application is not installed.\)
-   Software \[cmdb\_ci\_spkg\] \(If the SAM application is not installed.\)
-   Solaris Server \[cmdb\_ci\_solaris\_server\]
-   Storage Volume \[cmdb\_ci\_storage\_volume\]
-   UNIX Server \[cmdb\_ci\_unix\_server\]
-   VM Instance \[cmdb\_ci\_vm\_instance\]
-   Windows Server \[cmdb\_ci\_win\_server\]

For more information on where data is saved when pulling data from SolarWinds, see [CMDB classes targeted in Service Graph Connector for SolarWinds](../reference/cmdb-solarwinds-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

