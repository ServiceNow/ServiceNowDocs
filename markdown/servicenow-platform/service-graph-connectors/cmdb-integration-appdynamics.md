---
title: Service Graph Connector for Observability - AppDynamics
description: Use the Service Graph Connector for Observability - AppDynamics to ingest CMDB data from an AppDynamics installation using REST APIs. Push events from AppDynamics into ServiceNow with Event Management.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Observability - AppDynamics

Use the Service Graph Connector for Observability - AppDynamics to ingest CMDB data from an AppDynamics installation using REST APIs. Push events from AppDynamics into ServiceNow with Event Management.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Supported versions: AppDynamics version 20.3
-   Supported ServiceNow versions:
    -   Xanadu
    -   Yokohama
    -   Zurich

## Configuring a connection for the connector

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Observability - AppDynamics using SGC Central](../../sgc-central/task/sgcc-configure-appdynamics.md).

**Important:** Unless there are configuration issues, use SGC Central to configure the connection. The guided setup method for configuration is being deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring AppDynamics integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the AppDynamics data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The AppDynamics data sources include the following:

-   SG-AppDynamics Application Services
-   SG-AppDynamics Servers and Applications
-   SG-AppDynamics Server Tags
-   SG-AppDynamics Tier to Tier Relationship

For more information on where data is saved when pulling data from AppDynamics, see [CMDB classes targeted in Service Graph Connector for Observability - AppDynamics](../reference/cmdb-appdynamics-classes.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Additional resources

-   [Service Graph Connector for Observability AppDynamics](https://www.servicenow.com/community/cmdb-blog/service-graph-connector-for-observability-appdynamics/ba-p/2275530) article on the ServiceNow Community site
-   [How do I configure the AppDynamics Service Graph Connector?](https://www.servicenow.com/community/architect-articles/appdynamics-service-graph-connector/ta-p/2623395) article on the ServiceNow Community site

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

