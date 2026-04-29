---
title: API Service Graph Connector for Azure API Management
description: Use the ServiceNow API Service Graph Connector for Azure API Management to import API details from an Azure API Management application into the Configuration Management Database \(CMDB\).
locale: en-US
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

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Import data into a normalized data model for consistency across other technologies.

The API Insights workspace provides a centralized interface where you can analyze and interact with API data, without needing direct access to Azure API Management, enhancing visibility, governance, and collaboration across the API estate. To learn more, see [API Insights](../../api-insights/reference/api-insights.md).

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

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for Azure API Management using SGC Central](../../sgc-central/task/sgcc-configure-azure-api-mgmt.md).

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

[Azure API Management](../reference/api-sgc-azure-mgmt-tables.md#section_f35_vtj_4bc)[Azure Subscription](../reference/api-sgc-azure-mgmt-tables.md#section_gl3_dbk_h2c)

[Cloud Service Account](../reference/api-sgc-azure-mgmt-tables.md#section_fbj_tbk_h2c)

[Resource Group](../reference/api-sgc-azure-mgmt-tables.md#section_t1n_yzj_h2c)

[DNS Alias](../reference/api-sgc-azure-mgmt-tables.md#section_egg_qhb_1fc)

</td></tr><tr><td>

Managed API

</td><td>

SGA Azure Managed API \[sn\_azure\_api\_gw\_sga\_azure\_managed\_api\]

</td><td>

[Managed API](../reference/api-sgc-azure-mgmt-tables.md#section_bfw_xtj_4bc)

</td></tr><tr><td>

API Frontend Backend

</td><td>

SGA Azure API Frontend Backend \[sn\_azure\_api\_gw\_sga\_azure\_api\_frontend\_backend\_import\]

</td><td>

[API Frontend](../reference/api-sgc-azure-mgmt-tables.md#section_lrd_wtj_4bc)[API Backend](../reference/api-sgc-azure-mgmt-tables.md#section_kkr_xtj_4bc)

</td></tr><tr><td>

API GraphQL Frontend Backend

</td><td>

SGA Azure API GraphQL Frontend Backend \[sn\_azure\_api\_gw\_sga\_azure\_api\_graphql\_frontend\_backend\]

</td><td>

[API Frontend](../reference/api-sgc-azure-mgmt-tables.md#section_lrd_wtj_4bc)[API Backend](../reference/api-sgc-azure-mgmt-tables.md#section_kkr_xtj_4bc)

</td></tr><tr><td>

API Consumer

</td><td>

SGA Azure API Consumer \[sn\_azure\_api\_gw\_sga\_azure\_api\_consumer\]

</td><td>

[API Consumer](../reference/api-sgc-azure-mgmt-tables.md#section_wyl_wtj_4bc)

</td></tr><tr><td>

API Product

</td><td>

SGA Azure API Product \[sn\_azure\_api\_gw\_sga\_azure\_api\_product\]

</td><td>

[API Product Bundle](../reference/api-sgc-azure-mgmt-tables.md#section_yqh_rzj_h2c)

</td></tr><tr><td>

API Consumer Subscription

</td><td>

SGA Azure API Consumer Subscription \[sn\_azure\_api\_gw\_sga\_azure\_api\_subscription\]

</td><td>

[API Consumer Subscription](../reference/api-sgc-azure-mgmt-tables.md#section_xxg_pbk_h2c)

</td></tr><tr><td>

API Tag

</td><td>

API Tag \[sn\_azure\_api\_gw\_api\_tag\]

</td><td>

[Key Value](../reference/api-sgc-azure-mgmt-tables.md#section_yzv_j3b_1fc)

</td></tr><tr><td>

API Consumer Access

</td><td>

SGA Azure API Consumer Access \[sn\_azure\_api\_gw\_sga\_azure\_managed\_api\]

</td><td>

[API Consumer Access](../reference/api-sgc-azure-mgmt-tables.md#section_d3b_1ck_h2c)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from an Azure API Management application, see [Target tables for storing API Service Graph Connector for Azure API Management data](../reference/api-sgc-azure-mgmt-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Record removal process

The connector supports soft deletion for CMDB CI classes only, meaning records are not permanently removed from the system. Instead, any CMDB CI records not discovered during the last scheduled job run are marked as **Non-Operational**.

