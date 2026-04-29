---
title: API Service Graph Connector for AWS API Gateway
description: Use the ServiceNow API Service Graph Connector for AWS API Gateway to import API details from an AWS API Gateway service into the Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Service Graph Connector for AWS API Gateway

Use the ServiceNow® API Service Graph Connector for AWS API Gateway to import API details from an AWS API Gateway service into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Import data into a normalized data model for consistency across other technologies.

The API Insights workspace provides a centralized interface where you can analyze and interact with API data, without needing direct access to AWS API Gateway, enhancing visibility, governance, and collaboration across the API estate. To learn more, see [API Insights](../../api-insights/reference/api-insights.md).

## Supported ServiceNow versions

-   Xanadu
-   Yokohama
-   Zurich

## Use cases

You can use the API Service Graph Connector for AWS API Gateway to:

-   Maintain an end-to-end inventory of defined APIs, identifying what APIs are published, used, and by whom.
-   Track APIs from customer-facing endpoints to the underlying services, identifying impacted endpoints when services change or fail and creating incidents for reported issues.
-   Address vulnerabilities and security incidents related to API endpoints, and create compliance requirements to measure against.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for AWS API Gateway using SGC Central](../../sgc-central/task/sgcc-configure-aws-api-gateway.md).

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

[AWS API Gateway](../reference/api-sgc-aws-gateway-tables.md#section_ecv_wtj_4bc)[DNS Alias](../reference/api-sgc-aws-gateway-tables.md#section_y24_451_lgc)

[Managed API](../reference/api-sgc-aws-gateway-tables.md#section_bfw_xtj_4bc)

[Key Value](../reference/api-sgc-aws-gateway-tables.md#section_glk_m55_32c)

</td></tr><tr><td>

Managed API V2

</td><td>

SGA-AWS Managed API V2 \[sn\_aws\_api\_gw\_int\_sga\_aws\_managed\_api\_v2\]

</td><td>

[Managed API](../reference/api-sgc-aws-gateway-tables.md#section_bfw_xtj_4bc)[AWS API Gateway](../reference/api-sgc-aws-gateway-tables.md#section_ecv_wtj_4bc)

[DNS Alias](../reference/api-sgc-aws-gateway-tables.md#section_y24_451_lgc)

[Key Value](../reference/api-sgc-aws-gateway-tables.md#section_glk_m55_32c)

</td></tr><tr><td>

Frontend Backend REST

</td><td>

SGA-AWS Frontend-Backend REST \[sn\_aws\_api\_gw\_int\_sga\_aws\_frontend\_backend\_rest\]

</td><td>

[API Backend](../reference/api-sgc-aws-gateway-tables.md#section_kkr_xtj_4bc)[API Frontend](../reference/api-sgc-aws-gateway-tables.md#section_lrd_wtj_4bc)

</td></tr><tr><td>

Backend V2

</td><td>

SGA-AWS Backend V2 \[sn\_aws\_api\_gw\_int\_sga\_aws\_backend\_v2\]

</td><td>

[API Backend](../reference/api-sgc-aws-gateway-tables.md#section_kkr_xtj_4bc)

</td></tr><tr><td>

Frontend V2

</td><td>

SGA-AWS Frontend V2 \[sn\_aws\_api\_gw\_int\_sga\_aws\_frontend\_v2\]

</td><td>

[API Frontend](../reference/api-sgc-aws-gateway-tables.md#section_lrd_wtj_4bc)

</td></tr><tr><td>

Deployment Rest

</td><td>

SGA-AWS API Gateway Deployment Rest \[sn\_aws\_api\_gw\_int\_sga\_aws\_api\_gateway\_deployment\_rest\]

</td><td>

[API Deployment](../reference/api-sgc-aws-gateway-tables.md#section_hyq_ttj_4bc)

</td></tr><tr><td>

Deployment V2

</td><td>

SGA-AWS API Gateway Deployment V2 \[sn\_aws\_api\_gw\_int\_sga\_aws\_api\_gateway\_deployment\_v2\]

</td><td>

[API Deployment](../reference/api-sgc-aws-gateway-tables.md#section_hyq_ttj_4bc)

</td></tr><tr><td>

Consumer

</td><td>

SGA-AWS Consumers \[sn\_aws\_api\_gw\_int\_sga\_aws\_consumers\]

</td><td>

[API Consumer](../reference/api-sgc-aws-gateway-tables.md#section_wyl_wtj_4bc)

</td></tr><tr><td>

Policies

</td><td>

SGA-AWS API Gateway Policies \[sn\_aws\_api\_gw\_int\_sga\_aws\_api\_gateway\_policies\]

</td><td>

[API Policy](../reference/api-sgc-aws-gateway-tables.md#section_f35_vtj_4bc)

</td></tr><tr><td>

API Consumer Access

</td><td>

SGA-AWS-API-Consumer-Access \[sn\_aws\_api\_gw\_int\_sga\_aws\_api\_consumer\_access\]

</td><td>

[API Consumer Access](../reference/api-sgc-aws-gateway-tables.md#section_mh5_cv5_32c)

</td></tr></tbody>
</table>When you complete setting up the connection, you can configure the integration to periodically pull data from an AWS API Gateway service. For information on where data is saved when pulling data from an AWS API Gateway service, see [Target tables for storing API Service Graph Connector for AWS API Gateway data](../reference/api-sgc-aws-gateway-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Record removal process

The connector supports soft deletion for CMDB CI classes only, meaning records are not permanently removed from the system. Instead, any CMDB CI records not discovered during the last scheduled job run are marked as **Non-Operational**.

