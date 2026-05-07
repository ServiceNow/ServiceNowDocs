---
title: Create an Oracle metadata collector
description: Create a collector to import metadata from Oracle.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Oracle metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create an Oracle metadata collector

Create a collector to import metadata from Oracle.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](../concept/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the Oracle collector](prepare-to-run-oracle-collector.md#).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **Oracle**.

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

7.  Select from **Collect all schemas** or **Specify which schema to collect** to configure the schema collection options.

    |Field|Description|
    |-----|-----------|
    |Collect all schemas|
    |Collect all schemas|Catalog all schemas to which the user has access.|
    |Exclude Schema|Name or regular expression of the database schema to be excluded.|
    |Include Information Schema|Include the database's Information Schema in catalog collection.|
    |Specify which schema to collect|
    |Specify which schema to collect|Catalog only the specified schemas.|
    |Schema|Name of the database schema to catalog.|

8.  Configure the connection information.

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

Name of the database to connect to. Specify multiple databases by adding one value per line. If not specified, the collector harvests metadata from all databases.

</td></tr><tr><td>

Excluded database

</td><td>

Name or regular expression indicating databases not to catalog when the Database field is empty.**Note:** This parameter is ignored if the Database field is specified.

</td></tr></tbody>
</table>9.  Configure the statistics and sampling options.

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

</td></tr></tbody>
</table>10. Configure the harvesting scope and limits options.

    |Field|Description|
    |-----|-----------|
    |Database is an Oracle SID|Indicate that the database is actually an Oracle SID.|
    |Oracle JDBC Connection Timezone|Specify whether the default timezone of JVM should be used as the Oracle JDBC connection timezone.|
    |Enable Sample String Values collection|Enable harvesting of sample values and histograms for columns containing string data.|
    |Exclude system functions|Exclude system functions from metadata collection.|

11. Configure the connection and reliability options.

<table id="table_jml_1bc_l3c"><thead><tr><th>

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

Use Oracle Autonomous Database

</td><td>

Option to connect to an Autonomous Database.When this option is enabled:

-   Enter the service name as the value for the Database parameter. For example, g0404\_ktest\_high.adb.oraclecloud.com
-   Enter the host name as the value for the Server parameter. For example, adb.us-chicago-1.oraclecloud.com


</td></tr><tr><td>

Oracle Autonomous Database Connection String

</td><td>

The connection string for an Autonomous Database. The connection string should be in the format: jdbc:oracle:thin:@&lt;host&gt;:&lt;port&gt;/&lt;service\_name&gt; or jdbc:oracle:thin:@\(address=\(protocol=tcps\)\(port=&lt;port&gt;\) \(host:&lt;host&gt;\)\)\(connect\_data=\(service\_name=&lt;service\_name&gt;\)\)\(security=\(ssl\_server\_dn\_match=yes\)\)\).**Note:** The collector connects to the Oracle Cloud instance using the value in the Oracle Autonomous Database Connection String field. However, the server, port, and database parameters are still required—they are used for IRI coining and to uniquely identify the database data assets within your catalog.

</td></tr><tr><td>

JDBC properties

</td><td>

JDBC driver properties to pass through to driver connection.

</td></tr><tr><td>

SQL parsing timeout

</td><td>

Timeout in seconds for SQL parsing during lineage collection. Default: 60

</td></tr></tbody>
</table>12. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](../concept/manage-data-catalog.md).

**Parent Topic:**[Oracle metadata collector](../concept/oracle-metadata-collector.md)

