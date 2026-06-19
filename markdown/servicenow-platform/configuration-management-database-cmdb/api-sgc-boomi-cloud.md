---
title: API Service Graph Connector for Boomi Cloud API Management
description: Use the ServiceNow API Service Graph Connector for Boomi Cloud API Management to import API details from a Boomi Cloud API Management application into the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/api-sgc-boomi-cloud.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Service Graph Connector for Boomi Cloud API Management

Use the ServiceNow® API Service Graph Connector for Boomi Cloud API Management to import API details from a Boomi Cloud API Management application into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Import data into a normalized data model for consistency across other technologies.

The API Insights workspace provides a centralized interface where you can analyze and interact with API data, without needing direct access to a Boomi Cloud API Management application, enhancing visibility, governance, and collaboration across the API estate. To learn more, see [API Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/api-insights/api-insights.md).

## Supported ServiceNow versions

-   Yokohama
-   Zurich
-   Australia

## Use cases

You can use the API Service Graph Connector for Boomi Cloud API Management to:

-   Maintain an end-to-end inventory of exposed and backend APIs, identifying what APIs are published, used, and by whom.
-   Track APIs from customer-facing endpoints to the underlying services, identifying impacted endpoints when services change or fail and creating incidents for reported issues.
-   Address vulnerabilities and security incidents related to API endpoints and create compliance requirements to measure against.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The SGC Central view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for Boomi Cloud API Management using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sgcc-configure-boomi-cloud.md).

## Data mapping

Data from the Boomi Cloud API Management data sources is mapped and transformed into the CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from a Boomi Cloud API Management application.

The following table lists the data sources in the order they run, the staging tables, and the target tables as CMDB CI and non-CMDB classes for a Boomi Cloud API Management application.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

APIs

</td><td>

API Component \[sn\_boomi\_api\_component\]

</td><td>

[Managed API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-boomi-cloud-tables.md)[Boomi API Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-boomi-cloud-tables.md)

[API Frontend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-boomi-cloud-tables.md)

[API Backend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-boomi-cloud-tables.md)

</td></tr><tr><td>

API Consumer

</td><td>

API Consumer \[sn\_boomi\_api\_consumer\]

</td><td>

[API Consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-boomi-cloud-tables.md)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from a Boomi Cloud API Management application, see [Target tables for storing API Service Graph Connector for Boomi Cloud API Management data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/api-sgc-boomi-cloud-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

