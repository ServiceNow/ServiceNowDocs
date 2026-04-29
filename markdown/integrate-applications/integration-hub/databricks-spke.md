---
title: Databricks Spoke
description: Retrieves details of warehouses, tables, schemas, and catalogs, and executes SQL statements in Databricks from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Databricks Spoke

Retrieves details of warehouses, tables, schemas, and catalogs, and executes SQL statements in Databricks from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for these versions of Databricks, but may be compatible with later versions:

|Action category|Databricks version|
|---------------|------------------|
|Unity Catalog Management|API version 2.1|
|SQL Management|API version 2.0|

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Databricks spoke provides sample subflows to demonstrate automating tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Look up Catalogs|Retrieves list of all catalogs.|
|Look up Schemas|Retrieves list of all schemas from a specific catalog.|
|Look up Tables|Retrieves list of all tables from a specific schema in a catalog.|
|Sample - Execute Databricks SQL Statement|Executes a SQL statement on Databricks and returns the result columns and data array.|

## Spoke actions

The Databricks spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_tp4_k3n_k3c"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="4">

SQL Management

</td><td>

Execute SQL Statement

</td><td>

Executes the provided SQL statement.

</td></tr><tr><td>

Look up Execution Status

</td><td>

Retrieves the execution status of a SQL statement.

</td></tr><tr><td>

Look up Result Chunk by Index

</td><td>

Retrieves a specific chunk of the result set for a SQL statement by chunk index.**Note:** If the data you want to retrieve is more than 5MB, modify the default value of the system property **glide.pf.rest.response\_payload\_max\_size** and increase it as per your requirement.

</td></tr><tr><td>

Look up Warehouses Stream

</td><td>

Retrieves a list of SQL warehouses.

</td></tr><tr><td rowspan="3">

Unity Catalog Management

</td><td>

Look up Catalogs

</td><td>

Retrieves details of the required number of catalogs.**Note:** To retrieve list of all catalogs, use the Look up Catalogs subflow.

</td></tr><tr><td>

Look up Schemas

</td><td>

Retrieves details of the required number of schemas from a specific catalog.**Note:** To retrieve list of all schemas from a specific catalog, use the Look up Schemas subflow.

</td></tr><tr><td>

Look up Tables

</td><td>

Retrieves details of the required number of tables from a specific schema in a catalog.**Note:** To retrieve list of all tables from a specific schema in a catalog, use the Look up Tables subflow.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

