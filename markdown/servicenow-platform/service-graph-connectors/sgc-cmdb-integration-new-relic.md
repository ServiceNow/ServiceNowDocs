---
title: Service Graph Connector for Observability - New Relic
description: Use the Service Graph Connector for Observability - New Relic to ingest CMDB data from a New Relic installation using REST APIs. Push events from New Relic into ServiceNow with Event Management.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Observability - New Relic

Use the Service Graph Connector for Observability - New Relic to ingest CMDB data from a New Relic installation using REST APIs. Push events from New Relic into ServiceNow with Event Management.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   New Relic version: Last tested on July 01, 2025
-   Supported ServiceNow versions:
    -   Xanadu
    -   Yokohama
    -   Zurich

## Configuring a connection for the connector

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Observability - New Relic using SGC Central](../../sgc-central/task/sgcc-configure-new-relic-integ.md).

**Important:** Unless there are configuration issues, use SGC Central to configure the connection. The guided setup method for configuration is being deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Observability New Relic integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the New Relic data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The following data sources are included for New Relic:

-   SG-New Relic Application Services
-   SG-New Relic Applications
-   SG-New Relic Disks
-   SG-New Relic Hosts
-   SG\_New Relic Networks

When you complete setting up the connection, you can configure the integration to periodically pull data from the New Relic application. The data is loaded into the following staging tables:

-   SG-New Relic Applications \[sn\_newrelic\_integ\_sg\_new\_relic\_applications\]
-   SG-New Relic Application Services \[sn\_newrelic\_integ\_application\_services\]
-   SG-New Relic Disks \[sn\_newrelic\_integ\_disks\]
-   SG-New Relic Hosts \[sn\_newrelic\_integ\_hosts\]
-   SG\_New Relic Networks \[sn\_newrelic\_integ\_networks\]

The data is then inserted into the following target tables:

-   Application \[cmdb\_ci\_appl\]
-   Application service \[cmdb\_ci\_service\_calculated\]
-   Disk \[cmdb\_ci\_disk\]
-   IP Address\[cmdb\_ci\_ip\_address\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Running Process \[cmdb\_running\_process\]
-   Server \[cmdb\_ci\_server\]
-   Software Installation \[cmdb\_sam\_sw\_install\] \(If the Software Asset Management \(SAM\) application is installed.\)
-   Software Instance \[cmdb\_software\_instance\] \(If the SAM application is not installed.\)
-   Software \[cmdb\_ci\_spkg\] \(If the SAM application is not installed.\)

For more information on where data is saved when pulling data from New Relic, see [CMDB classes targeted in Service Graph Connector for Observability - New Relic](../reference/sgc-cmdb-new-relic-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## System property

The **sn\_newrelic\_integ.alerts\_for\_unmatched\_ci.enabled** system property determines whether to ingest events that don't have a matching CMDB CI class. Set the value of this system property to `true` to ingest unmatched events. The default value is `false`.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

