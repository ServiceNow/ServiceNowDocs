---
title: Service Graph Connector for Tanium Endpoints
description: Use the Service Graph Connector for Tanium Endpoints to integrate the data discovered by Tanium into your ServiceNow instance to support various use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-integration-tanium-endpoints.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Tanium Endpoints

Use the Service Graph Connector for Tanium Endpoints to integrate the data discovered by Tanium into your ServiceNow instance to support various use cases.

**Important:** The Service Graph Connector for Tanium Endpoints populates the Computer class with user-facing endpoints, and doesn't import data from the Server child class. Use this connector if you don't require Server data. If you require Server data, use the Service Graph Connector for Tanium.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Yokohama Patch 4
-   Zurich
-   Australia

## Use cases

The Service Graph Connector for Tanium Endpoints enables your IT Asset Management \(ITAM\) use cases. The following examples describe how you can use the Service Graph Connector for Tanium Endpoints:

-   Maintain an accurate and up-to-date inventory of Tanium configuration items \(CIs\) in the CMDB.
-   Identify and assess dependencies between CIs discovered by Tanium.
-   Identify data quality issues, reconcile inconsistencies, and manage incidents and changes on discovered CIs.
-   Schedule periodic synchronization of Tanium data to keep your CMDB up to date.

## Configuring a connection for the connector

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Tanium Endpoints using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgcc-configure-tanium-endpoints.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Tanium Endpoints integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

**Related topics**  


[Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md)

[Configure Service Graph Connector for Tanium Endpoints using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgcc-configure-tanium-endpoints.md)

[CMDB classes targeted in Service Graph Connector for Tanium Endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

[Data mapping for Service Graph Connector for Tanium Endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-data-mapping-tanium-endpoints.md)

