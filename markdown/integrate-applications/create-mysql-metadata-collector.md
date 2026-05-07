---
title: Create a MySQL metadata collector
description: Create a collector to import metadata from MySQL.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [MySQL metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a MySQL metadata collector

Create a collector to import metadata from MySQL.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](../concept/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the MySQL collector](prepare-to-run-mysql-collector.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **MySQL**.

5.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field cannot be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

6.  Configure the authentication options.

    |Field|Description|
    |-----|-----------|
    |Username|Username to use to connect to the database.|
    |Password|Password of the databsase user.|

7.  Configure the connection information.

<table id="table_mtg_br2_h3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server

</td><td>

Hostname of the database server to connect to.

</td></tr><tr><td>

Server port

</td><td>

Port of the database server \(if not the default\).

</td></tr><tr><td>

Database

</td><td>

Name of the database to connect to. Specify multiple databases by adding one value per line.

</td></tr><tr><td>

Excluded database

</td><td>

Name or regular expression indicating databases not to catalog when the Database field is empty.**Note:** This parameter is ignored if the Database field is specified.

</td></tr></tbody>
</table>8.  Configure the statistics and sampling options.

<table id="table_ocr_gc4_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable column statistics collection

</td><td>

Enable harvesting of column statistics \(that is, data profiling\).**Note:** Enabling profiling can increase the collector’s runtime, as the collector must read table data to generate profiling metadata.

</td></tr><tr><td>

Target sample size for column statistics

</td><td>

Number of rows sampled for computation of column statistics and string-value histograms. For example, to sample 1000 rows, set the parameter as: 1000.Default: 100000

</td></tr><tr><td>

Disable Lineage collection

</td><td>

Skip harvesting of intra-database lineage metadata.

</td></tr><tr><td>

Disable Extended Metadata collection

</td><td>

Skip harvesting of extended metadata for data asset types such as database, schema, table, columns functions, stored procedures, user defined types, synonyms. Basic metadata for these data asset types will still be harvested.

</td></tr><tr><td>

Enable Sample String Values collection

</td><td>

Enable sampling and storage of sample values for string-valued columns.

</td></tr><tr><td>

Exclude system functions

</td><td>

Exclude harvesting of built-in system functions.

</td></tr></tbody>
</table>9.  Configure the connection and reliability options.

<table id="table_yhb_plp_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server environment

</td><td>

Friendly name for the environment in which your database server runs when the server name is localhost. Helps differentiate it from other environments.

</td></tr><tr><td>

Database ID

</td><td>

Unique identifier for this database. Used to generate the database ID when the database name is not sufficiently unique.

</td></tr><tr><td>

JDBC properties

</td><td>

JDBC driver properties to pass through to driver connection.

</td></tr><tr><td>

SQL parsing timeout

</td><td>

Timeout in seconds for SQL parsing during lineage collection. Default: 60

</td></tr></tbody>
</table>10. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](../concept/manage-data-catalog.md).

**Parent Topic:**[MySQL metadata collector](../concept/mysql-metadata-collector.md)

