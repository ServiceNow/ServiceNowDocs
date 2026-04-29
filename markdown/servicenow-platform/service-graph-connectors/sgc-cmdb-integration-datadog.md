---
title: Service Graph Connector for Observability - Datadog
description: Use the Service Graph Connector for Observability - Datadog to ingest CMDB data from a Datadog installation using REST APIs. Push events from Datadog into ServiceNow with Event Management.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Observability - Datadog

Use the Service Graph Connector for Observability - Datadog to ingest CMDB data from a Datadog installation using REST APIs. Push events from Datadog into ServiceNow with Event Management.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Supported ServiceNow versions:

-   Yokohama
-   Zurich
-   Australia

## Guided setup

The guided setup for the Service Graph Connector for Observability - Datadog provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure Service Graph Connector for Observability - Datadog](../task/sgc-configure-datadog-integration.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Observability Datadog integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Datadog data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The Datadog data source includes SGO-Datadog Hosts \[sn\_datadog\_integra\_datadog\_hosts\].

For more information on where data is saved when pulling data from Datadog, see [CMDB classes targeted in Service Graph Connector for Observability - Datadog](../reference/sgc-cmdb-datadog-classes.md).

When you complete setting up the connection, the data from Datadog is automatically loaded into staging tables and then inserted into the following target tables:

-   Cloud DataBase \[cmdb\_ci\_cloud\_database\]
-   Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]
-   Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Key Value \[cmdb\_key\_value\]
-   Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Server \[cmdb\_ci\_server\]

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

[Configure Service Graph Connector for Observability - Datadog](../task/sgc-configure-datadog-integration.md)

[CMDB classes targeted in Service Graph Connector for Observability - Datadog](../reference/sgc-cmdb-datadog-classes.md)

[Accessing the connection details of Service Graph Connector for Observability - Datadog](sgc-datadog-conn.md#)

