---
title: API Service Graph Connector for Apigee Edge
description: Use the ServiceNow API Service Graph Connector for Apigee Edge to import API details from an Apigee Edge application into the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-07-20"
reading_time_minutes: 3
breadcrumb: [API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Service Graph Connector for Apigee Edge

Use the ServiceNow® API Service Graph Connector for Apigee Edge to import API details from an Apigee Edge application into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Key features

Import organizations, managed APIs, frontends and backends, product bundles, and consumer subscription data from an Apigee Edge application into a normalized data model for consistency across other technologies.

## Supported ServiceNow versions

-   Yokohama
-   Zurich
-   Australia

## Use cases

You can use the API Service Graph Connector for Apigee Edge to:

-   Maintain an end-to-end inventory of exposed and backend APIs, identifying what APIs are published, used, and by whom.
-   Track APIs from customer-facing endpoints to the underlying services, identifying impacted endpoints when services change or fail and creating incidents for reported issues.
-   Discover and inventory Apigee Edge organizations as API gateways within the CMDB.
-   Track API product bundles and their relationships to managed APIs.
-   Monitor API consumer subscriptions and consumer access details for governance and analysis.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The SGC Central view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for Apigee Edge using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sgcc-configure-apigee-edge.md).

## Data mapping

Data from the Apigee Edge data sources is mapped and transformed into the CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from an Apigee Edge application.

The following table lists the data sources in the order they run, the staging tables, and the target tables as CMDB CI and non-CMDB classes for an Apigee Edge application.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

Organization

</td><td>

Organization \[sn\_apigee\_edge\_organization\]

</td><td>

[Apigee API Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)

</td></tr><tr><td>

Managed API

</td><td>

Managed API \[sn\_apigee\_edge\_managed\_api\]

</td><td>

[Managed API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)[API Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)

[DNS Alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)

</td></tr><tr><td>

Frontend Backends

</td><td>

Frontend Backends \[sn\_apigee\_edge\_frontend\_backends\]

</td><td>

[API Backend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)[API Frontend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)

</td></tr><tr><td>

API Product

</td><td>

API Product \[sn\_apigee\_edge\_api\_product\]

</td><td>

[API Product Bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)

</td></tr><tr><td>

API Consumer Subscription

</td><td>

API Consumer Subscription \[sn\_apigee\_edge\_api\_consumer\_subscription\]

</td><td>

[API Consumer Subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)

</td></tr><tr><td>

API Consumer Access

</td><td>

API Consumer Access \[sn\_apigee\_edge\_api\_consumer\_access\]

</td><td>

[API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)[API Consumer Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)

</td></tr><tr><td>

Consumer

</td><td>

Consumer \[sn\_apigee\_edge\_consumer\]

</td><td>

[API Consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from an Apigee Edge application, see [Target tables for storing API Service Graph Connector for Apigee Edge data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

