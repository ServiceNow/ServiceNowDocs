---
title: Databricks metadata collector
description: The Databricks metadata collector provides read-only access to metadata from an external Databricks account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Databricks metadata collector

The Databricks metadata collector provides read-only access to metadata from an external Databricks account.

The collector harvests metadata from data assets in Databricks Hive Metadata, Unity Catalog \(including Delta Lake\), Workflows, and Notebooks.

## Metadata cataloged

The Databricks collector catalogs the following information.

<table id="table_bqt_dpz_qhc"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Columns

</td><td>

Name, Description, JDBC type, Column Type, Is Nullable, Default Value, Column size, Column index

 Extended metadata: Tags

 **Note:** Deprecated columns and any lineage related to these deprecated columns are not cataloged.

</td></tr><tr><td>

Table

</td><td>

Name, Description, Schema, Primary key, Foreign key

 Extended metadata: Tags, Owner, Type, Creation date, Last Modified, Location, Provider, Version, Size, File Count, Partition Columns, Properties

</td></tr><tr><td>

Model

</td><td>

Name, Owner, Description, Created By, Created At, Last Modified By, Last Modified At, Securable Kind, Securable Type

</td></tr><tr><td>

Views

</td><td>

Name, Description, SQL definition, Tags

</td></tr><tr><td>

Schema

</td><td>

Name

 Extended metadata: Tags

</td></tr><tr><td>

Database

</td><td>

Type, Name, Server, Port, Environment, JDBC URL

 Extended metadata: Tags

</td></tr><tr><td>

Notebook

</td><td>

Notebook ID, Path, Language Type \(SQL, Python, Scala, R\)

</td></tr><tr><td>

Function

</td><td>

Name, Description, Function Type

</td></tr><tr><td>

Job

</td><td>

Title, Description, Creator, Created At, Job run as, Format, Max Concurrent Runs, Notification On Start, Timeouts \(sec\), Notification On Success, Schedule, Git Source, Notification on Failure, Tags, List of tasks, List of clusters

</td></tr><tr><td>

Cluster

</td><td>

Name, Description, Node Type ID, Driver Node Type ID, Spark Version, Number of Workers, Autoscale Max Workers, Autoscale Min Workers, AWS Attributes, Tags

</td></tr><tr><td>

Task

</td><td>

Task Key, Type of Task \(Notebook, dbt, Spark jar, Python script, Python wheel, Pipeline task, SQL\), Task timeout, Retry interval, Cluster used by the task, Max retries, Depends on, Libraries, Notifications \(On start, On success, On failure\), Notebook File Path, Notebook Source, Notebook Parameters, Spark Jar Main Class Name, Spark Jar Parameters, Python Script File path, Python Script Parameters, Spark Submit Parameters, Pipeline ID, Pipeline Full Refresh, Python Wheel Package Name, Python Wheel Entry Point, Python Wheel Parameters, SQL Warehouse, SQL Query ID, SQL Dashboard ID, SQL Alert ID, Dbt Project Directory, Dbt Profiles Directory, Dbt warehouse, Dbt catalog, Dbt schema, Dbt commands

</td></tr><tr><td>

External Location

</td><td>

Name, External URL, Description, Data Source Type, Created Date, Created By, Owner

</td></tr><tr><td>

Storage Credential

</td><td>

Name, Description, Credential, Created Date, Created By, Owner

</td></tr><tr><td>

Volume

</td><td>

Name, Description, Type, Owner, Created By, Created At, Last Modified By, Last Modified At, Metastore ID

</td></tr><tr><td>

Materialized View

</td><td>

Name, SQL Definition, Created, Last Modified

</td></tr><tr><td>

Metric View

</td><td>

Name, Description, YAML Definition, Source Table, Source Table Type, Filter, Created, Last Modified

</td></tr></tbody>
</table>## Relationships between objects

The harvested metadata includes catalog pages for the following data asset types. Each catalog page has a relationship to the other related data asset types.

<table id="table_dqf_nxl_rhc"><thead><tr><th>

Data asset page

</th><th>

Relationships

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Columns contained in Table

</td></tr><tr><td>

Schema

</td><td>

-   Database that contains Schema
-   Table that is part of Schema

</td></tr><tr><td>

Database

</td><td>

Schema contained in Database

</td></tr><tr><td>

Columns

</td><td>

Table containing Column

</td></tr><tr><td>

Job

</td><td>

-   Clusters used by tasks in Job
-   Tasks contained within Job

</td></tr><tr><td>

Cluster

</td><td>

-   Cluster contained in job
-   Task using Cluster

</td></tr><tr><td>

Task

</td><td>

-   Job containing Task
-   Cluster used by Task
-   Tasks depending on Task

</td></tr><tr><td>

Notebook

</td><td>

-   Folder containing Notebook
-   Task sourcing data from Notebook

</td></tr><tr><td>

Folder

</td><td>

-   Folders contained in Folder
-   Notebooks contained in Folder

</td></tr><tr><td>

External Location

</td><td>

-   Uses storage credential
-   Connects to datasource \(S3 bucket, S3 Object, Azure container or Azure blob\)

</td></tr><tr><td>

Storage Credential

</td><td>

Used by External Location

</td></tr><tr><td>

Model

</td><td>

-   Registered in schema
-   Stored in data assets \(S3 Bucket, S3 Object\)

</td></tr><tr><td>

Volume

</td><td>

-   Contained within schema
-   Stored in data assets \(S3 Bucket, S3 Object\)

</td></tr><tr><td>

Materialized View

</td><td>

-   Schema that contains Materialized Views
-   Columns that are part of Materialized Views

</td></tr><tr><td>

Metric View

</td><td>

-   Schema that contains Metric Views
-   Columns that are part of Metric Views

</td></tr></tbody>
</table>## Lineage for Databricks

The following lineage information is collected by the Databricks collector.

**Note:** The collector does not support lineage for SQL statements defined via variable statements.

<table id="table_esh_q54_13c"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

Column in view

</td><td>

The collector identifies the associated column in an upstream view or table for both Hive metastore and Unity Catalog: -   Where the data is sourced from
-   That sort the rows via ORDER BY
-   That filter the rows via WHERE/HAVING
-   That aggregate the rows via GROUP BY

 **Note:** Deprecated columns and any lineage related to these deprecated columns are not cataloged.

</td></tr><tr><td>

Notebook

</td><td>

Tasks that reference Notebook. \(Only if Databricks Unity Catalog is enabled\).

</td></tr><tr><td>

Table

</td><td>

-   The collector identifies the upstream and downstream tables and their external locations \(S3 and ADLS Gen2 data assets\) along with the intermediate Job.
-   The collector harvests the Databricks table lineage to S3 object.

</td></tr></tbody>
</table>## Authentication supported

The Databricks collector supports Personal access token authentication and Oauth service principal authentication.

-   **[Prepare to run the Databricks collector](../task/prepare-to-run-the-databricks-collector.md#)**  
Complete authentication and permission configuration tasks before running the Databricks metadata collector.
-   **[Create a Databricks metadata collector](../task/create-databricks-metadata-collector.md)**  
Create a collector to import metadata from Databricks.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

