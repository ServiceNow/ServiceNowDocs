---
title: API Service Graph Connector for AWS API Gateway
description: Use the ServiceNow API Service Graph Connector for AWS API Gateway to import API details from an AWS API Gateway service into the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Service Graph Connector for AWS API Gateway

Use the ServiceNow® API Service Graph Connector for AWS API Gateway to import API details from an AWS API Gateway service into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Import data into a normalized data model for consistency across other technologies.

The API Insights workspace provides a centralized interface where you can analyze and interact with API data, without needing direct access to AWS API Gateway, enhancing visibility, governance, and collaboration across the API estate. To learn more, see [API Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/api-insights/api-insights.md).

## Supported ServiceNow versions

-   Yokohama
-   Zurich
-   Australia

## Use cases

You can use the API Service Graph Connector for AWS API Gateway to:

-   Maintain an end-to-end inventory of defined APIs, identifying what APIs are published, used, and by whom.
-   Track APIs from customer-facing endpoints to the underlying services, identifying impacted endpoints when services change or fail and creating incidents for reported issues.
-   Address vulnerabilities and security incidents related to API endpoints, and create compliance requirements to measure against.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for AWS API Gateway using SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/sgcc-configure-aws-api-gateway.md).

## Data mapping

Data from the AWS API Gateway data sources is mapped and transformed into the CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the CMDB using the Identification and Reconciliation Engine \(IRE\).

The following table lists the data sources in the order they run, the staging tables, and the target tables as CMDB CI and non-CMDB classes for an AWS API Gateway service.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

Managed API Rest

</td><td>

SGA-AWS Managed API Rest \[sn\_aws\_api\_gw\_int\_api\_gateway\_managed\_api\_import\_set\]

</td><td>

[AWS API Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)[DNS Alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

[Managed API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

Managed API V2

</td><td>

SGA-AWS Managed API V2 \[sn\_aws\_api\_gw\_int\_sga\_aws\_managed\_api\_v2\]

</td><td>

[Managed API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)[AWS API Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

[DNS Alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

Frontend Backend REST

</td><td>

SGA-AWS Frontend-Backend REST \[sn\_aws\_api\_gw\_int\_sga\_aws\_frontend\_backend\_rest\]

</td><td>

[API Backend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)[API Frontend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

Backend V2

</td><td>

SGA-AWS Backend V2 \[sn\_aws\_api\_gw\_int\_sga\_aws\_backend\_v2\]

</td><td>

[API Backend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

Frontend V2

</td><td>

SGA-AWS Frontend V2 \[sn\_aws\_api\_gw\_int\_sga\_aws\_frontend\_v2\]

</td><td>

[API Frontend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

Deployment Rest

</td><td>

SGA-AWS API Gateway Deployment Rest \[sn\_aws\_api\_gw\_int\_sga\_aws\_api\_gateway\_deployment\_rest\]

</td><td>

[API Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

Deployment V2

</td><td>

SGA-AWS API Gateway Deployment V2 \[sn\_aws\_api\_gw\_int\_sga\_aws\_api\_gateway\_deployment\_v2\]

</td><td>

[API Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

Consumer

</td><td>

SGA-AWS Consumers \[sn\_aws\_api\_gw\_int\_sga\_aws\_consumers\]

</td><td>

[API Consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

Policies

</td><td>

SGA-AWS API Gateway Policies \[sn\_aws\_api\_gw\_int\_sga\_aws\_api\_gateway\_policies\]

</td><td>

[API Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr><tr><td>

API Consumer Access

</td><td>

SGA-AWS-API-Consumer-Access \[sn\_aws\_api\_gw\_int\_sga\_aws\_api\_consumer\_access\]

</td><td>

[API Consumer Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md)

</td></tr></tbody>
</table>When you complete setting up the connection, you can configure the integration to periodically pull data from an AWS API Gateway service. For information on where data is saved when pulling data from an AWS API Gateway service, see [Target tables for storing API Service Graph Connector for AWS API Gateway data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/api-sgc-aws-gateway-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

## Record removal process

The connector supports soft deletion for CMDB CI classes only, meaning records are not permanently removed from the system. Instead, any CMDB CI records not discovered during the last scheduled job run are marked as **Non-Operational**.

