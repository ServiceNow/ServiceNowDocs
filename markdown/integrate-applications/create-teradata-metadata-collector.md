---
title: Create a Teradata metadata collector
description: Create a collector to import metadata from Teradata.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-teradata-metadata-collector.html
release: australia
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 3
breadcrumb: [Teradata metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a Teradata metadata collector

Create a collector to import metadata from Teradata.

## Before you begin

-   A MID Server is set up for the collectors. For more information, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mid-server-for-metadata-collectors-dc.md).
-   All prerequisite tasks are complete. For more information, see [Prepare to run the Teradata Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prepare-to-run-teradata-collector.md).

Role required: connection-admin or admin.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub \[Omitted image "wdf-connect-hub-icon.png"\] Alt text: Connect Hub icon icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **Teradata**.

5.  From the Connection type list, select one of the following:

    1.  Select **New connection** to configure a new connection.

    2.  Select **Existing connection** to reuse an existing connection and select an existing connection from the **Connections** list.

        The configuration form is filled with details from the existing connection. The name is appended with the word Copy and sensitive details like password aren't copied.

6.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field can't be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

7.  Configure the connection properties.

    |Field|Description|
    |-----|-----------|
    |Server|Hostname of the database server to connect to.|
    |Server port|Port of the database server, if not the default.|

8.  Configure the authentication options.

    | | |
    |---|---|
    |User name|Username for authenticating with the database server.|
    |Password|Password for authenticating with the database server.|

9.  Configure the database options.

<table id="table_bwq_bvt_rjc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Include databases

</td><td>

Name of the database to connect to. To add multiple databases, select **Add**. **Note:** If this property is not specified, the collector harvests metadata from all databases. Use the optional **Excluded databases** parameter to exclude specific databases.

</td></tr><tr><td>

Excluded databases

</td><td>

Regular expressions indicating databases not to catalog. Use when the **Include databases** parameter is not set — the collector then harvests metadata from all databases, and this parameter excludes specific ones. **Note:** This parameter is ignored if the **Include databases** parameter is specified. To use **Excluded databases**, do not set the **Database** parameter.

</td></tr></tbody>
</table>10. Configure the advanced options.

<table id="table_lsp_cvt_rjc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Enable column statistics collection

</td><td>

Whether to enable harvesting of column statistics, that is, data profiling. **Note:** Enabling this feature may extend the running time of the collector because the collector requires access to table data to gather profiling metadata.

</td></tr><tr><td>

Target sample size for column statistics

</td><td>

Target number of rows to sample from tables.

</td></tr><tr><td>

Disable lineage collection

</td><td>

Whether to skip harvesting of intra-database lineage metadata.

</td></tr><tr><td>

Disable extended metadata collection

</td><td>

Whether to skip harvesting of extended metadata for resource types such as database, schema, table, columns, functions, stored procedures, user-defined types, and synonyms. Basic metadata for these resource types is still harvested.

</td></tr><tr><td>

Exclude system functions

</td><td>

Whether to exclude system functions.

</td></tr><tr><td>

Server environment

</td><td>

Friendly name for the environment in which the database server runs. Use this field when the server name is `localhost` to differentiate it from other environments.

</td></tr><tr><td>

Database ID

</td><td>

Unique identifier for this database, used to generate the ID for the database. Provide this value only if the database name used for the connection does not uniquely identify the database.

</td></tr><tr><td>

JDBC properties

</td><td>

JDBC driver properties to pass to the driver connection, in `name=value` format.

</td></tr><tr><td>

SQL parsing timeout

</td><td>

Timeout in seconds for SQL parsing during lineage collection. The default is 60.

</td></tr></tbody>
</table>11. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. The collector is ready to connect to the source system and harvest metadata.

## What to do next

After the collector is created, perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-data-catalog.md).

**Parent Topic:**[Teradata metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/teradata-metadata-collector.md)

