---
title: Getting started with Service Graph Connectors
description: Service Graph Connectors, including API Service Graph Connectors, are predefined integrations that ingest third-party data and API data into the Configuration Management Database \(CMDB\) from various domains, such as security, servers, software or monitoring, Internet of Things \(IoT\), and cloud.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-12-09"
reading_time_minutes: 8
breadcrumb: [Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Getting started with Service Graph Connectors

Service Graph Connectors, including API Service Graph Connectors, are predefined integrations that ingest third-party data and API data into the Configuration Management Database \(CMDB\) from various domains, such as security, servers, software or monitoring, Internet of Things \(IoT\), and cloud.

**Important:** See [Service Graph Connectors](cmdb-sgc-available.md) and [API Service Graph Connectors](api-sgc-available.md) for a list of connectors provided by ServiceNow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Service Graph Connectors overview

The following video provides an overview of Service Graph Connectors.

Service Graph Connectors

As a purpose-built app, you can use a Service Graph Connector, including an API Service Graph Connector, to maintain the quality and consistency of third-party data in your CMDB.

You can use the following connector types:

-   **Service Graph Connectors**

    A Service Graph Connector imports and integrates third-party data into CMDB and non-CMDB tables. For a list of Service Graph Connectors, see [Service Graph Connectors](cmdb-sgc-available.md).

-   **API Service Graph Connectors**

    An API Service Graph Connector imports and integrates third-party API data into CMDB and non-CMDB tables. For a list of API Service Graph Connectors, see [API Service Graph Connectors](api-sgc-available.md).

-   **Partner-built connectors**

    Service Graph Connectors can be built by partners and vendors. For a list of partner-built connectors, see the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/integrations?freeTrial=service_graph_certified&offeredby=partners) website.


The connectors also make sure that third-party data is mapped to the right locations in your CMDB as specified by the Common Service Data Model \(CSDM\). The CSDM enables ServiceNow products to use the data and increases reporting accuracy. For more information on CSDM, see [Common Service Data Model](../../csdm-implementation/concept/csdm-landing-page.md).

The Service Graph Connectors, including API Service Graph Connectors, manage the configuration data pipeline in the following steps:

1.  Ingest the data by identifying class, attribute, and data sources by using the identification rules.
2.  Standardize the data to comply with your CMDB.
3.  Reconcile the data into a single coherent picture by using the reconciliation rules.
4.  Ingest the data into your CMDB.

You can track the status and processing results of all installed integrations using the SGC Central view within the CMDB Workspace or integrations dashboard provided with the Integration Commons for CMDB store app. For more information, see [SGC Central](../../sgc-central/reference/sgcc-landing.md), [Integration Commons for CMDB](integration-commons-for-cmdb.md), and [CMDB Integrations Dashboard](cmdb-integ-dashboard.md#).

## Service Graph Connector user roles

Service Graph Connector users can be assigned specific roles to limit the assignment of the Administrator \(admin\) user role. The following roles are available for Service Graph Connector users.

<table id="table_dfz_zpp_4hc"><thead><tr><th>

User role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrator

</td><td>

Users with the admin role can install and upgrade Service Graph Connectors, including API Service Graph Connectors. Administrators can perform the following tasks:-   Create a connection and configure connection properties.
-   Monitor connections and data imports.
-   Manage connections.
-   Upgrade the connector.
-   Run background scripts.
-   Provide access to tables in the global scope.

</td></tr><tr><td>

SGC-admin

</td><td>

The sn\_cmdb\_int\_util.sgc\_admin user role has the second-highest level of permissions for Service Graph Connectors. SGC-admin users can perform the following tasks:-   Create, update, and delete connections.
-   Configure connectors using the guided setup.
-   Read and write the system properties that are used by the connectors.
-   Perform all operations that are allowed by other user roles that have lower levels of permission.

</td></tr><tr><td>

CMDB installation administrator

</td><td>

Users with the cmdb\_inst\_admin role can use [IntegrationHub ETL](integrationhub-etl.md) to create and customize integrations. CMDB installation administrators can perform the following tasks:-   Read all Service Graph Connector application modules.
-   Read and write the system properties that are used by the connectors.
-   Create, update, and delete custom tables.
-   Create, update, and delete scheduled imports and data sources.
-   Read records that are owned by other applications and are related to the functionality of Service Graph Connectors \(for instance, records in the em\_event table\).

</td></tr></tbody>
</table>## Using SGC Central for connectors

The Service Graph Connector Central application also called as SGC Central is available as a view in the CMDB Workspace. The application enables you to discover and install Service Graph Connectors, including API Service Graph Connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. The SGC Central application also ensures that connectors remain supported and up-to-date with certified partners.

The SGC Central application minimizes customization and accelerates time to value with intuitive setup options and playbook-guided connector deployment. If the playbook experience isn’t available for a connector, you can follow the guided setup provided with the connector.

To learn more, see [SGC Central](../../sgc-central/reference/sgcc-landing.md).

## Using connectors

By using Service Graph Connectors and API Service Graph Connectors, you can mandate data governance and design practices. Examples of mandated practices using connectors include:

-   Consistently associating data with specific CI types. For instance, IP addresses are assigned to network interfaces rather than a mix of interfaces and servers. Ensuring that ServiceNow products know where to find third-party data. For more information, see [CMDB classifications and class dependency](c_CMDBClassifications.md).
-   Using the Identification and Reconciliation \(IRE\) engine to identify and classify data correctly before it’s loaded into the CMDB. Helping prevent duplicate CIs and ensuring that attribute values are consistent across multiple data sources.

    For information on the IRE-related rules used in Service Graph Connectors, see the following topics:

    -   [CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md)
    -   [Identification rules](c_IdentificationRules.md)
    -   [Reconciliation rules](../reference/r_ReconciliationRulesPrinciples.md)
    -   [Create an IRE data source rule](../task/create-ire-data-source-rule.md)
    -   [Detecting duplicate CIs](id-detect-dup-ci.md)
    -   [Create a data refresh rule](../task/create-datasource-staleness-rule.md)
    -   [Create an identification inclusion rule](../task/create-id-inclusion-rule.md)
-   Using the IntegrationHub ETL functionality so that data is transformed and loaded in the fastest and most efficient manner. For more information, see [IntegrationHub ETL](integrationhub-etl.md).

## Resolving connector issues

You can use the Now Assist for Configuration Management Database \(CMDB\) application to resolve any issues or perform a general analysis on a connector installed on your instance. See [Fix SGC import set issues with the Now Assist SGC diagnosis skill](../task/now-assist-cmdb-sgc-diagnose.md).

