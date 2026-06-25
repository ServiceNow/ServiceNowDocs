---
title: Service Graph Connector for Observability - Dynatrace SaaS
description: Use the Service Graph Connector for Observability - Dynatrace SaaS to integrate the data discovered by Dynatrace into your ServiceNow instance to support various use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-integration-observability-dynatrace-saas.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-06-03"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Observability - Dynatrace SaaS

Use the Service Graph Connector for Observability - Dynatrace SaaS to integrate the data discovered by Dynatrace into your ServiceNow instance to support various use cases.

**Important:** The Service Graph Connector for Observability - Dynatrace SaaS is designed for the Dynatrace SaaS \(3rd‑generation\) platform and leverages DQL-based APIs and the Grail architecture to import data from Dynatrace into the CMDB. If you're in a Dynatrace managed \(self‑hosted\) or legacy SaaS environment, you should use the Service Graph Connector for Observability - Dynatrace.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Yokohama Patch 11
-   Zurich Patch 4
-   Australia

## Use cases

The following examples describe how you can use the Service Graph Connector for Observability - Dynatrace SaaS:

-   Maintain an accurate and up-to-date inventory of Dynatrace configuration items \(CIs\) in the CMDB.
-   Automatically build and maintain service topology maps showing dependencies between services, processes, and hosts.
-   Link Dynatrace alerts to the correct CI in the ServiceNow CMDB so that incidents inherit the service context, and the correct team is alerted without manual intervention.
-   Schedule periodic synchronization of Dynatrace data to keep your CMDB up to date.

## Configuring a connection for the connector

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Observability - Dynatrace SaaS using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgcc-configure-dynatrace-saas.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Observability - Dynatrace SaaS integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

**Related topics**  


[Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md)

[Configure Service Graph Connector for Observability - Dynatrace SaaS using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgcc-configure-dynatrace-saas.md)

[CMDB classes targeted in Service Graph Connector for Observability - Dynatrace SaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

[Data mapping for Service Graph Connector for Observability - Dynatrace SaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-data-mapping-dynatrace-saas.md)

