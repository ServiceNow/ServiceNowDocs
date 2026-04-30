---
title: API Service Graph Connector for Apigee X
description: Use the ServiceNow API Service Graph Connector for Apigee X to import API proxy details from an Apigee X application into the Configuration Management Database \(CMDB\).
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Service Graph Connector for Apigee X

Use the ServiceNow® API Service Graph Connector for Apigee X to import API proxy details from an Apigee X application into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Import data into a normalized data model for consistency across other technologies.

The API Insights workspace provides a centralized interface where you can analyze and interact with API data, without needing direct access to Apigee X, enhancing visibility, governance, and collaboration across the API estate. To learn more, see [API Insights](../../api-insights/reference/api-insights.md).

## Supported ServiceNow versions

-   Yokohama
-   Zurich
-   Australia

## Use cases

You can use the API Service Graph Connector for Apigee X to:

-   Maintain an end-to-end inventory of exposed and backend APIs, identifying what APIs are published, used, and by whom.
-   Track APIs from customer-facing endpoints to the underlying services, identifying impacted endpoints when services change or fail and creating incidents for reported issues.
-   Address vulnerabilities and security incidents related to API endpoints, and create compliance requirements to measure against.

## Important information for upgrading API Service Graph Connector for Apigee X

If you’re an existing customer using production instances, reach out to Now Support before upgrading to API Service Graph Connector for Apigee X v2.3.0. This upgrade alters source native keys that can impact Source \[sys\_object\_source\] table records. Coordinating with Now Support helps to prevent duplicate record creation.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for Apigee X using SGC Central](../../sgc-central/task/sgcc-configure-apigee-x.md).

## Data mapping

Data from the Apigee X data sources is mapped and transformed into the CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from an Apigee X application.

The following table lists the data sources in the order that they run, the staging tables, and the target tables as CMDB CI and non-CMDB classes for an Apigee X application.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

Apigee Organization

</td><td>

SGA Apigee X Apigee Organization \[sn\_apigee\_x\_apigee\_organization\]

</td><td>

[Google Organization Project](../reference/api-sgc-apigee-x-tables.md#section_tkk_p4d_3cc)[Apigee API Gateway](../reference/api-sgc-apigee-x-tables.md#section_zws_54d_3cc)

</td></tr><tr><td>

Managed API

</td><td>

SGA Apigee X Managed API \[sn\_apigee\_x\_sga\_apigee\_x\_managed\_api\]

</td><td>

[Managed API](../reference/api-sgc-apigee-x-tables.md#section_bfw_xtj_4bc)[API Deployment](../reference/api-sgc-apigee-x-tables.md#section_f35_vtj_4bc)

[Apigee API Gateway](../reference/api-sgc-apigee-x-tables.md#section_zws_54d_3cc)

</td></tr><tr><td>

API Consumer

</td><td>

SGA Apigee X API Consumer \[sn\_apigee\_x\_sga\_apigee\_x\_api\_consumer\]

</td><td>

[API Consumer](../reference/api-sgc-apigee-x-tables.md#section_wyl_wtj_4bc)

</td></tr><tr><td>

API Frontend Backend

</td><td>

SGA Apigee X Frontend Backend \[sn\_apigee\_x\_sga\_apigee\_x\_frontend\_backend\]

</td><td>

[API Frontend](../reference/api-sgc-apigee-x-tables.md#section_lrd_wtj_4bc)[API Backend](../reference/api-sgc-apigee-x-tables.md#section_kkr_xtj_4bc)

</td></tr><tr><td>

API Product

</td><td>

SGA Apigee X API Product \[sn\_apigee\_x\_sga\_apigee\_x\_api\_product\]

</td><td>

[API Product Bundle](../reference/api-sgc-apigee-x-tables.md#section_blq_jn3_h2c)[Key Value](../reference/api-sgc-apigee-x-tables.md#section_ddb_rn3_h2c)

</td></tr><tr><td>

API Consumer Subscription

</td><td>

SGA Apigee X API Consumer Subscription \[sn\_apigee\_x\_sga\_apigee\_x\_api\_consumer\_subscription\]

</td><td>

[API Consumer Subscription](../reference/api-sgc-apigee-x-tables.md#section_mfm_n43_h2c)[Key Value](../reference/api-sgc-apigee-x-tables.md#section_ddb_rn3_h2c)

</td></tr><tr><td>

API Consumer Access

</td><td>

SGA Apigee X API Consumer Access \[sn\_apigee\_x\_sga\_apigee\_x\_api\_consumer\_access\]

</td><td>

[API Consumer Access](../reference/api-sgc-apigee-x-tables.md#section_jll_ym3_h2c)

</td></tr><tr><td>

GCP Organization

</td><td>

SGA Apigee X Organization \[sn\_apigee\_x\_sga\_apigee\_x\_organization\]

</td><td>

[Cloud Organizations](../reference/api-sgc-apigee-x-tables.md#section_ecv_wtj_4bc)

</td></tr><tr><td>

GCP Folder

</td><td>

SGA Apigee X Folder \[sn\_apigee\_x\_sga\_apigee\_x\_folder\]

</td><td>

[Google Organization Folder](../reference/api-sgc-apigee-x-tables.md#section_fyl_ymd_3cc)

</td></tr><tr><td>

GCP Project

</td><td>

SGA Apigee X Project \[sn\_apigee\_x\_sga\_apigee\_x\_project\]

</td><td>

[Google Organization Project](../reference/api-sgc-apigee-x-tables.md#section_tkk_p4d_3cc)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from an Apigee X application, see [Target tables for storing API Service Graph Connector for Apigee X data](../reference/api-sgc-apigee-x-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Record removal process

The connector supports soft deletion for CMDB CI classes only, meaning records aren’t permanently removed from the system. Instead, any CMDB CI records not discovered during the last scheduled job run are marked as **Non-Operational**.

