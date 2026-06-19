---
title: API Service Graph Connector for Azure API Management
description: Use the ServiceNow API Service Graph Connector for Azure API Management to import API details from an Azure API Management application into the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Service Graph Connector for Azure API Management

Use the ServiceNow® API Service Graph Connector for Azure API Management to import API details from an Azure API Management application into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Import data into a normalized data model for consistency across other technologies.

The API Insights workspace provides a centralized interface where you can analyze and interact with API data, without needing direct access to Azure API Management, enhancing visibility, governance, and collaboration across the API estate. To learn more, see [API Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/api-insights/api-insights.md).

## Supported ServiceNow versions

-   Yokohama
-   Zurich
-   Australia

## Use cases

You can use the API Service Graph Connector for Azure API Management to:

-   Maintain an end-to-end inventory of exposed and backend APIs, identifying what APIs are published, used, and by whom.
-   Track APIs from customer-facing endpoints to the underlying services, identifying impacted endpoints when services change or fail and creating incidents for reported issues.
-   Address vulnerabilities and security incidents related to API endpoints, and create compliance requirements to measure against.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for Azure API Management using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sgcc-configure-azure-api-mgmt.md).

**Important:** Unless there are configuration issues, use SGC Central to configure the connection. The guided setup method for configuration is being deprecated.

## Data mapping

Data from the Azure API Management data sources is mapped and transformed into the CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from an Azure API Management application.

The following table lists the data sources in the order they run, the staging tables, and the target tables as CMDB CI and non-CMDB classes for an Azure API Management application.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

API Management Services

</td><td>

SGA Azure API Management \[sn\_azure\_api\_gw\_sga\_azure\_api\_management\]

</td><td>

[Azure API Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)[Azure Subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

[Resource Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

[DNS Alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr><tr><td>

Managed API

</td><td>

SGA Azure Managed API \[sn\_azure\_api\_gw\_sga\_azure\_managed\_api\]

</td><td>

[Managed API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr><tr><td>

API Frontend Backend

</td><td>

SGA Azure API Frontend Backend \[sn\_azure\_api\_gw\_sga\_azure\_api\_frontend\_backend\_import\]

</td><td>

[API Frontend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)[API Backend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr><tr><td>

API GraphQL Frontend Backend

</td><td>

SGA Azure API GraphQL Frontend Backend \[sn\_azure\_api\_gw\_sga\_azure\_api\_graphql\_frontend\_backend\]

</td><td>

[API Frontend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)[API Backend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr><tr><td>

API Consumer

</td><td>

SGA Azure API Consumer \[sn\_azure\_api\_gw\_sga\_azure\_api\_consumer\]

</td><td>

[API Consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr><tr><td>

API Product

</td><td>

SGA Azure API Product \[sn\_azure\_api\_gw\_sga\_azure\_api\_product\]

</td><td>

[API Product Bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr><tr><td>

API Consumer Subscription

</td><td>

SGA Azure API Consumer Subscription \[sn\_azure\_api\_gw\_sga\_azure\_api\_subscription\]

</td><td>

[API Consumer Subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr><tr><td>

API Tag

</td><td>

API Tag \[sn\_azure\_api\_gw\_api\_tag\]

</td><td>

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr><tr><td>

API Consumer Access

</td><td>

SGA Azure API Consumer Access \[sn\_azure\_api\_gw\_sga\_azure\_managed\_api\]

</td><td>

[API Consumer Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from an Azure API Management application, see [Target tables for storing API Service Graph Connector for Azure API Management data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-azure-mgmt-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

## Record removal process

The connector supports soft deletion for CMDB CI classes only, meaning records are not permanently removed from the system. Instead, any CMDB CI records not discovered during the last scheduled job run are marked as **Non-Operational**.

