---
title: API Service Graph Connector for MuleSoft
description: Use the ServiceNow API Service Graph Connector for MuleSoft to import API details from a MuleSoft Anypoint Platform application into the Configuration Management Database \(CMDB\).
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-01-20"
reading_time_minutes: 3
breadcrumb: [API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API Service Graph Connector for MuleSoft

Use the ServiceNow® API Service Graph Connector for MuleSoft to import API details from a MuleSoft Anypoint Platform application into the Configuration Management Database \(CMDB\).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Key features

Import data into a normalized data model for consistency across other technologies.

The API Insights workspace provides a centralized interface where you can analyze and interact with API data, without needing direct access to a MuleSoft Anypoint Platform application, enhancing visibility, governance, and collaboration across the API estate. To learn more, see [API Insights](../../api-insights/reference/api-insights.md).

## Supported ServiceNow versions

-   Xanadu
-   Yokohama
-   Zurich

## Use cases

You can use the API Service Graph Connector for MuleSoft to:

-   Maintain an end-to-end inventory of exposed and backend APIs, identifying what APIs are published, used, and by whom.
-   Create relationships between API managers, runtime deployments, and gateway instances to understand service dependencies and identify impact when services change or fail.
-   Track all managed APIs across multiple MuleSoft organizations and environments, identifying which APIs are active, deployed, and their operational status.
-   Address vulnerabilities and security incidents related to API endpoints and create compliance requirements.
-   Identify impacted endpoints when backend services change or fail, enabling proactive incident management and faster resolution times.

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the CMDB Workspace. The SGC Central view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure API Service Graph Connector for MuleSoft using SGC Central](../../sgc-central/task/sgcc-configure-mulesoft.md).

## Data mapping

Data from the MuleSoft Anypoint Platform data sources is mapped and transformed into the CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from a MuleSoft Anypoint Platform application.

The following table lists the data sources in the order they run, the staging tables, and the target tables as CMDB CI and non-CMDB classes for a MuleSoft Anypoint Platform application.

<table id="table_s3s_dns_zxb" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

Gateway

</td><td>

Gateway \[sn\_mulesoft\_gateway\]

</td><td>

[Anypoint API Gateway](../reference/api-sgc-mulesoft-tables.md#section_d3q_45r_whc)

</td></tr><tr><td>

API Manager

</td><td>

Managed API \[sn\_mulesoft\_managed\_api\]

</td><td>

[Managed API](../reference/api-sgc-mulesoft-tables.md#section_uww_y5r_whc)[Key Value \[cmdb\_key\_value\]](../reference/api-sgc-mulesoft-tables.md#section_w23_ywr_whc)

</td></tr><tr><td>

Frontend And Backend

</td><td>

Frontend And Backend \[sn\_mulesoft\_frontend\_and\_backend\]

</td><td>

[Frontend](../reference/api-sgc-mulesoft-tables.md#section_ayw_2vr_whc)[Backend](../reference/api-sgc-mulesoft-tables.md#section_zgm_nwr_whc)

</td></tr><tr><td>

API Deployments

</td><td>

API Deployments \[sn\_mulesoft\_api\_deployments\]

</td><td>

[API Deployment](../reference/api-sgc-mulesoft-tables.md#section_scn_rwr_whc)[Data Service Instance](../reference/api-sgc-mulesoft-tables.md#section_cnb_wwr_whc)

</td></tr></tbody>
</table>For more information on where data is saved when pulling data from a MuleSoft Anypoint Platform application, see [Target tables for storing API Service Graph Connector for MuleSoft data](../reference/api-sgc-mulesoft-tables.md).

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

