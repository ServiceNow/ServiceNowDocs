---
title: API Service Graph Connector for Kong Gateway
description: Use the ServiceNow API Service Graph Connector for Kong Gateway to import API details from a Kong Gateway application into the Configuration Management Database \(CMDB\).
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Service Graph Connector for Kong Gateway

Use the ServiceNow® API Service Graph Connector for Kong Gateway to import API details from a Kong Gateway application into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Import data into a normalized data model for consistency across other technologies.

The API Insights workspace provides a centralized interface where you can analyze and interact with API data, without needing direct access to Kong Gateway, enhancing visibility, governance, and collaboration across the API estate. To learn more, see [API Insights](../../api-insights/reference/api-insights.md).

## Supported ServiceNow versions

-   Yokohama
-   Zurich
-   Australia

## Use cases

You can use the API Service Graph Connector for Kong Gateway to:

-   Maintain an end-to-end inventory of exposed and backend APIs, identifying what APIs are published, used, and by whom.
-   Track APIs from customer-facing endpoints to the underlying services, identifying impacted endpoints when services change or fail and creating incidents for reported issues.
-   Address vulnerabilities and security incidents related to API endpoints, and create compliance requirements.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The SGC Central view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for Kong Gateway using SGC Central](../../sgc-central/task/sgcc-configure-kong-gateway.md).

**Note:** You can also include a Prometheus connection and map it to the Kong Gateway connection during setup for importing Kong Gateway metrics data using the Prometheus plugin. To learn more about the Prometheus plugin, see [Prometheus](https://developer.konghq.com/plugins/prometheus) on the Kong Developer documentation site.

## Data mapping

Data from the Kong Gateway data sources is mapped and transformed into the CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from a Kong Gateway application.

The following table lists the data sources in the order they run, the staging tables, and the target tables as CMDB CI and non-CMDB classes for a Kong Gateway application.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-Kong Gateway

</td><td>

SG-Kong Gateway \[sn\_kong\_integ\_sg\_kong\_gateway\]

</td><td>

[Kong Gateway](../reference/api-sgc-kong-gateway-tables.md#section_ecv_wtj_4bc)

</td></tr><tr><td>

SG-Kong Workspaces

</td><td>

SG-Kong Workspaces \[sn\_kong\_integ\_sg\_kong\_workspaces\]

</td><td>

[Kong Workspace](../reference/api-sgc-kong-gateway-tables.md#section_zws_54d_3cc)

</td></tr><tr><td>

SG-Kong Load Balancers

</td><td>

SG-Kong Load Balancers \[sn\_kong\_integ\_sg\_kong\_lbs\]

</td><td>

[Kong Load Balancer](../reference/api-sgc-kong-gateway-tables.md#section_fyl_ymd_3cc)

</td></tr><tr><td>

SG-Kong Targets

</td><td>

SG-Kong Targets \[sn\_kong\_integ\_sg\_kong\_targets\]

</td><td>

[Kong Target](../reference/api-sgc-kong-gateway-tables.md#section_tkk_p4d_3cc)[Key Value](../reference/api-sgc-kong-gateway-tables.md#section_vjj_ks5_s2c)

</td></tr><tr><td>

SG-Kong Services

</td><td>

SG-Kong Services \[sn\_kong\_integ\_sg\_kong\_services\]

</td><td>

[Managed API](../reference/api-sgc-kong-gateway-tables.md#section_bfw_xtj_4bc)[API Backend](../reference/api-sgc-kong-gateway-tables.md#section_kkr_xtj_4bc)

[Key Value](../reference/api-sgc-kong-gateway-tables.md#section_vjj_ks5_s2c)

</td></tr><tr><td>

SG-Kong Routes

</td><td>

SG-Kong Routes \[sn\_kong\_integ\_sg\_kong\_routes\]

</td><td>

[API Frontend](../reference/api-sgc-kong-gateway-tables.md#section_lrd_wtj_4bc)

</td></tr><tr><td>

SG-Kong Consumers

</td><td>

SG-Kong Consumers \[sn\_kong\_integ\_sg\_kong\_consumers\]

</td><td>

[API Consumer](../reference/api-sgc-kong-gateway-tables.md#section_wyl_wtj_4bc)

</td></tr><tr><td>

SG-Kong Plugins

</td><td>

SG-Kong Plugins \[sn\_kong\_integ\_sg\_kong\_plugins\]

</td><td>

[API Policy](../reference/api-sgc-kong-gateway-tables.md#section_f35_vtj_4bc)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from a Kong Gateway application, see [Target tables for storing API Service Graph Connector for Kong Gateway data](../reference/api-sgc-kong-gateway-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

