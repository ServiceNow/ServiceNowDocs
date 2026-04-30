---
title: Service Graph Connector for Akamai API Security
description: Use the Service Graph Connector for Akamai API Security to integrate the APIs discovered by Akamai into your ServiceNow instance to support various API management use cases.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-10-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Akamai API Security

Use the Service Graph Connector for Akamai API Security to integrate the APIs discovered by Akamai into your ServiceNow instance to support various API management use cases.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

-   Supported ServiceNow versions:
    -   Xanadu
    -   Yokohama
    -   Zurich
-   Supported Akamai API Security REST APIs:
    -   /api/v3/apis
    -   /api/v3/sources
    -   /auth/token

## Use cases

The Service Graph Connector for Akamai API Security brings data into the new API Insights capability of the ServiceNow platform, enabling the management of different APIs in one instance. The connector adds information discovered by Akamai API Security to the API Component CI class.

The Service Graph Connector for Akamai API Security populates attributes that are security- and risk-related, such as the request and response data types, whether an API endpoint is internet-facing, and the type of authentication used for the endpoint. These data points enable risk and security use cases to be implemented for API security.

## Configuring a connection for the connector

Use the SGC Central view in the Service Graph Workspace or CMDB Workspace to install the connector and configure the connection. The view enables you to install and discover connectors and to manage the full life cycle of creating, editing, monitoring, and debugging connections. For instructions, see [Configure Service Graph Connector for Akamai API Security using SGC Central](../../sgc-central/task/sgcc-configure-akamai-integ.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring Akamai API Security integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## Data mapping

Data from the Akamai API Security data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

The following table lists the data sources, the staging tables, and the target tables as CMDB CI and non-CMDB classes for Akamai API Security.

<table id="table_ngb_mss_ygc" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

Sources

</td><td>

sn\_akamai\_api\_sec\_akamai\_sources

</td><td>

Akamai API Security Sources \[sn\_akamai\_source\]

</td></tr><tr><td>

API Component

</td><td>

sn\_akamai\_api\_sec\_sga\_akamai\_api\_component

</td><td>

[API Component \[cmdb\_ci\_api\_component\]](../reference/cmdb-akamai-classes.md#section_vfb_r4n_ygc)[Key Value \[cmdb\_key\_value\]](../reference/cmdb-akamai-classes.md#section_uxt_r4n_ygc)

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](integrationhub-etl.md) for more information.

## Scheduled script for full data load

The Service Graph Connector for Akamai API Security supports both full load and delta load data ingestion methods. A full data load retrieves all API-related data and populates the corresponding CMDB tables.​ Delta loads fetch only the data that changed since the previous execution.

During the initial scheduled data import, a full data load is executed. Subsequent data imports perform delta loads​.

To run a full data load on a recurring basis, customize the execution schedule of the **Reset Last Run Datetime for SG-Akamai** scheduled script based on your requirements. To open the Scheduled Script Executions table, enter `sysauto_script.list` in the navigation filter.

## Additional resource

[Management API Reference](https://docs.nonamesecurity.com/docs/management-api-references)

**Related topics**  


[Service Graph Connectors](cmdb-sgc-available.md)

[Configure Service Graph Connector for Akamai API Security using SGC Central](../../sgc-central/task/sgcc-configure-akamai-integ.md)

[CMDB classes targeted in Service Graph Connector for Akamai API Security](../reference/cmdb-akamai-classes.md)

