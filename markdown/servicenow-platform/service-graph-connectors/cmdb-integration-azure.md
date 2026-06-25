---
title: Service Graph Connector for Microsoft Azure
description: Use the Service Graph Connector for Microsoft Azure to pull data from Microsoft Azure into your CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/cmdb-integration-azure.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Microsoft Azure

Use the Service Graph Connector for Microsoft Azure to pull data from Microsoft Azure into your CMDB.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Supported ServiceNow versions:

-   Yokohama
-   Zurich
-   Australia

## Use cases

The following are examples on how you can use the Service Graph Connector:

-   Visibility into cloud resources, relationships, and state.
-   Service ITAM/SAM outcomes through deep discovery of applications.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for Microsoft Azure using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgcc-configure-azure-integ.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecation.

## Important information for upgrading Service Graph Connector for Microsoft Azure

After you upgrade to the latest version of the Service Graph Connector for Microsoft Azure, you must run a full data load. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sgc-intro.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Microsoft Azure integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

## Event-based discovery

The Service Graph Connector for Microsoft Azure works with event-based discovery. Events that are pulled from Azure can create and update CIs that were brought by the Service Graph Connector for Microsoft Azure.

## Additional resource

[How do I configure the Azure Service Graph Connector?](https://www.servicenow.com/community/cmdb-articles/azure-service-graph-connector-version-1-12/ta-p/3308034)

**Related topics**  


[Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md)

[Configure Service Graph Connector for Microsoft Azure using the guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/configure-azure-integration.md)

[Data mapping for Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-data-mapping-azure.md)

[CMDB classes targeted in Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-azure-classes.md)

[Service Graph Connector for Microsoft Azure properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-azure-props.md)

[Configuring data synchronization in Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-azure-data-sync.md)

[Enabling VM insights for collecting Azure data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-azure-vm-insights.md)

[Setting up multiple connections in Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-azure-multi.md)

