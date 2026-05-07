---
title: Create a Databricks metadata collector
description: Create a collector to import metadata from Databricks.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Databricks metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a Databricks metadata collector

Create a collector to import metadata from Databricks.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](../concept/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the Databricks collector](prepare-to-run-the-databricks-collector.md#).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **Databricks**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field cannot be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

6.  Enter the Databricks configuration details.

    |Field|Description|
    |-----|-----------|
    |Server|Hostname of the database server to connect to.|

7.  Choose between **Collect all schemas** and **Specify which schema to collect** to configure the schema collection options.

    |Field|Description|
    |-----|-----------|
    |Collect all schemas|
    |Collect all schemas|Catalog all schemas to which the user has access.|
    |Exclude Schema|Name or regular expression of the database schema to be excluded.|
    |Include Information Schema|Include the database's Information Schema in catalog collection.|
    |Specify which schema to collect|
    |Specify which schema to collect|Catalog only the specified schemas.|
    |Schema|Name of the database schema to catalog.|

8.  Enter the Databricks configuration details.

<table id="table_pjv_hr4_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server port

</td><td>

Port of the database server \(if not the default\).

</td></tr><tr><td>

Database

</td><td>

Name of the database to connect to. Specify multiple databases by adding one value per line.

</td></tr><tr><td>

Databricks HTTP Path

</td><td>

Databricks compute resources URL. See [Databricks documentation](https://docs.databricks.com/integrations/bi/jdbc-odbc-bi.html#odbc-configuration-and-connection-parameters) for details.

</td></tr><tr><td>

Excluded database

</td><td>

Name or regular expression for databases to exclude when the Database field is empty.**Note:** This parameter is ignored if the Database field is specified.

</td></tr></tbody>
</table>9.  Configure the server details and authentication options.

    |Field|Description|
    |-----|-----------|
    |Server details|
    | |Hostname of the database server to connect to.|
    |Authentication options|
    |Authenticate using personal access token|Option to authenticate using the Databricks personal access token. For details, see [Databricks documentation.](https://docs.databricks.com/dev-tools/api/latest/authentication.html)|
    |Authenticate using Databricks Service Principal|Option to authenticate using the Databricks service principal client ID and Databricks Service Principal Client Secret.|

10. Configure the statistics and sampling options.

<table id="table_ocr_gc4_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable column statistics collection

</td><td>

Enable harvesting of column statistics \(data profiling\).**Note:** Enabling profiling can increase the collector's runtime because the collector must read table data to generate profiling metadata.

</td></tr><tr><td>

Target sample size for column statistics

</td><td>

Number of rows sampled for computation of column statistics and string-value histograms. For example, to sample 1000 rows, set the parameter to 1000.Default: 100000

</td></tr><tr><td>

Disable Lineage collection

</td><td>

Skip harvesting of intra-database lineage metadata.

</td></tr><tr><td>

Disable Extended Metadata collection

</td><td>

Skip harvesting of extended metadata for data asset types such as database, schema, table, columns functions, stored procedures, user defined types, and synonyms. Basic metadata for these data asset types will still be harvested.

</td></tr></tbody>
</table>11. Configure the harvesting scope and limits options.

<table id="table_kbn_4lp_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable Harvesting Workflows

</td><td>

Skip harvesting of Databricks workflows and their lineage metadata.

</td></tr><tr><td>

Harvest Lineage from Other Schemas

</td><td>

Harvest lineage from other schemas.

</td></tr><tr><td>

Enable Sample String Values collection

</td><td>

Enable sampling and storage of sample values for string-valued columns.

</td></tr><tr><td>

Exclude system functions

</td><td>

Exclude harvesting of built-in Databricks system functions.

</td></tr><tr><td>

Disable Harvesting Notebook Content

</td><td>

Skip harvesting notebook content.

</td></tr><tr><td>

Page Size for Harvesting Queries

</td><td>

Specify the page size for harvesting queries.Default: 1000

</td></tr><tr><td>

Page Size for Databricks API Responses

</td><td>

Specify the page size for Databricks API response. Default: 100

</td></tr><tr><td>

Enable Metric Views Harvesting

</td><td>

Enable harvesting of metric views. Metric view information is extracted from a table's extended metadata and is available only when extended metadata harvesting is enabled.

</td></tr></tbody>
</table>12. Configure the connection and reliability options.

<table id="table_yhb_plp_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server environment

</td><td>

Friendly name for the environment where your database server runs when the server name is localhost. Helps differentiate it from other environments.

</td></tr><tr><td>

Database ID

</td><td>

Unique identifier for this database. Used to generate the database ID when the database name isn't sufficiently unique.

</td></tr><tr><td>

JDBC properties

</td><td>

JDBC driver properties to pass through to driver connection.

</td></tr><tr><td>

Max retries

</td><td>

The number of times the system retries a failed API call.Default: 5

</td></tr><tr><td>

Retry delay

</td><td>

The number of seconds to wait between retry attempts for a failed API call.Default: 2 seconds

</td></tr><tr><td>

Disable Model Collection

</td><td>

Skip harvesting machine learning models.

</td></tr><tr><td>

Databricks account ID

</td><td>

The Databricks account ID for Unity Catalog access.

</td></tr><tr><td>

External Workspace URL

</td><td>

The external workspace URL for cross-workspace access.

</td></tr><tr><td>

SQL parsing timeout

</td><td>

Timeout in seconds for SQL parsing during lineage collection. Default: 60

</td></tr></tbody>
</table>13. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](../concept/manage-data-catalog.md).

**Parent Topic:**[Databricks metadata collector](../concept/databricks-metadata-collector.md)

