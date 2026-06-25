---
title: Service Graph Connector for Observability - Dynatrace
description: Use the Service Graph Connector for Observability - Dynatrace to ingest CI data, events, metrics, and logs from Dynatrace into your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/cmdb-integration-dynatrace.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Observability - Dynatrace

Use the Service Graph Connector for Observability - Dynatrace to ingest CI data, events, metrics, and logs from Dynatrace into your ServiceNow instance.

**Important:** The Service Graph Connector for Observability - Dynatrace supports Dynatrace Classic \(v1/v2 APIs\) and is intended for Dynatrace managed \(self‑hosted\) or legacy SaaS environments. If you're using or upgrading to the latest Dynatrace 3rd-generation SaaS platform, you should use the new Service Graph Connector for Observability - Dynatrace SaaS.

The Service Graph Connector for Observability - Dynatrace provided by ServiceNow is different from the Service Graph Connector for Dynatrace provided by Dynatrace.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Supported versions:
    -   Minimum version supported: Dynatrace SaaS; Version 1.284
-   Supported ServiceNow versions:
    -   Yokohama
    -   Zurich
    -   Australia

## Important information for upgrading Service Graph Connector for Observability - Dynatrace

Before upgrading the Service Graph Connector for Observability - Dynatrace to version 1.10.0 or later, disable the reconciliation rules for tables extending the Application \[cmdb\_ci\_appl\] table. See the [Reconciliation rules\(ServiceNow, ServiceWatch\) on multiple table like Apache web server stopping other discovery source to update fields on those tables \[KB1649455\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649455) article in the Now Support Knowledge Base.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for Observability - Dynatrace using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgcc-configure-dynatrace.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecation.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Dynatrace integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md).

## Additional resources

-   [Introduction to Service Graph Connector for Observability Dynatrace](https://www.servicenow.com/community/cmdb-blog/introduction-to-service-graph-connector-for-observability/ba-p/2275131) article on the ServiceNow Community site
-   [How do I configure the Dynatrace Service Graph Connector?](https://www.servicenow.com/community/architect-articles/dynatrace-service-graph-connector/ta-p/2619549) article on the ServiceNow Community site

**Related topics**  


[Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md)

[Service Graph Connector for Observability - Dynatrace properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-dynatrace-props.md)

