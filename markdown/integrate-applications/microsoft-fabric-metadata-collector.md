---
title: Microsoft Fabric metadata collector
description: Provides read-only access to metadata from a Microsoft Fabric account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/microsoft-fabric-metadata-collector.html
release: australia
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 9
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Microsoft Fabric metadata collector

Provides read-only access to metadata from a Microsoft Fabric account.

The collector harvests metadata from Microsoft Fabric workspaces and their child resources, including items commonly found in Power BI.

## Metadata cataloged

The collector catalogs the following information.

<table id="table_x4s_xdx_gkc"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Workspaces

</td><td>

ID, Name, Description

</td></tr><tr><td>

Warehouses

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, Collation Type, Connection String, JDBC URL, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

Lakehouses

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, OneLake Tables Path, OneLake Files Path, Connection String, JDBC URL, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

Fabric Data Pipelines

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, Parameters, Variables, Endorsement \(Certified By, Endorsement Badge\), Refresh Schedule

</td></tr><tr><td>

Eventhouses

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, Endorsement \(Certified By, Endorsement Badge\), Ingestion Service URI, Query Service URI, State

</td></tr><tr><td>

Dataflows

</td><td>

ID, Name, Description, Last Modified Date, Refresh Schedule, Created By, Last Modified By, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

Dataflow Gen2

</td><td>

ID, Name, Description, Created By, Last Modified Date, Last Modified By, Endorsement \(Certified By, Endorsement Badge\), Refresh Schedule

</td></tr><tr><td>

Dataflow Gen2 CI/CD

</td><td>

ID, Name, Description, Created Date, Created By, Last Modified Date, Last Modified By, Endorsement \(Certified By, Endorsement Badge\), Refresh Schedule, State

</td></tr><tr><td>

Mirrored Databases

</td><td>

OneLake Tables Path, Mirroring Status

</td></tr><tr><td>

Fabric Mirrored Database Table

</td><td>

Name, Description, Table Mirroring Status Extended Metadata: Created Date, Modified Date

</td></tr><tr><td>

Fabric Delta Lakehouse Table

</td><td>

Name, Description, Created Date, Last Modified Date, ABFS File Path

</td></tr><tr><td>

Fabric Lakehouse Column

</td><td>

Name, Description, Column Type, Is Nullable, Column Size, Column Index, Decimal Digits, Partition Index

</td></tr><tr><td>

Notebooks

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, Definition, Endorsement \(Certified By, Endorsement Badge\), Refresh Schedule

</td></tr><tr><td>

Spark Job Definitions

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, Endorsement \(Certified By, Endorsement Badge\), Refresh Schedule

</td></tr><tr><td>

SQL Analytics Endpoints

</td><td>

ID, Name, Description, Last Modified Date, Created By, Modified By, Provisioning Status, Connection String, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

Lakehouse Folders

</td><td>

ID, Name, Description, Created Date, Last Modified Date, ABFS File Path

</td></tr><tr><td>

Lakehouse Files

</td><td>

ID, Name, Description, Created Date, Last Modified Date, ABFS File Path

</td></tr><tr><td>

Schemas

</td><td>

Name Extended Metadata: Created Date, Modified Date

</td></tr><tr><td>

Fabric Database Tables

</td><td>

Name, Description, Primary Key, ABFS File Path Extended metadata: Created date, Modified date

</td></tr><tr><td>

Database Columns

</td><td>

Name, Description, JDBC Type, Column Type, Is Nullable, Default Value, Key Type \(Primary, Foreign\), Column Size, Column Index, Decimal Digits

</td></tr><tr><td>

Views

</td><td>

Name, Description, SQL Definition

</td></tr><tr><td>

Reports

</td><td>

ID, Name, Description, Type, Preview Image \(supported for paginated reports\), Created Date, Last Modified Date, Created by, Modified by, External URL, Embed URL, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

Report Pages

</td><td>

Name, Is Hidden

</td></tr><tr><td>

Dashboards

</td><td>

ID, Name, External URL, Embed URL

</td></tr><tr><td>

Dashboard Tiles

</td><td>

Name, Embed URL

</td></tr><tr><td>

Semantic Models

</td><td>

ID, Title, Description, Created Date, Created By, External URL, Refresh Schedule

</td></tr><tr><td>

Data Sources

</td><td>

Name, Type, Connection Details

</td></tr><tr><td>

Fabric Logical Tables

</td><td>

Name, Description, Is Hidden, Is Entered Data, Expression

</td></tr><tr><td>

Fabric Calculated Tables

</td><td>

Name, Description, Is Hidden, Is Entered Data, Expression

</td></tr><tr><td>

Fabric Logical Columns

</td><td>

Name, Description, Data Type, Column Type, Is Hidden, Expression

</td></tr><tr><td>

Measures

</td><td>

Name, Description, Is Hidden, Expression

</td></tr><tr><td>

Data Pipeline Activity

</td><td>

Name, Description, Type, Inactivity Status, Activity Policy \(Retry, Timeout, Retry Interval In Secs, Secure Input, Secure Output\)

</td></tr><tr><td>

Data Pipeline Run

</td><td>

Start Time, End Time, Invoke Type, Run Status

</td></tr><tr><td>

Activity Run

</td><td>

Start Time, End Time, Run Status, Output Message, Error Message

</td></tr><tr><td>

Job Run

</td><td>

ID, Job Type, Start Time, End Time, Run Status, Invocation Type, Failure Reason

</td></tr><tr><td>

KQL Database

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, State, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

App

</td><td>

ID, Name, Description

</td></tr><tr><td>

Org App

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

GraphQL API

</td><td>

ID, Name, Description, GraphQL Api Definition, Created Date, Last Modified Date, Created By, Modified By, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

Refresh Schedule

</td><td>

ID, Frequency, Recurrence Interval, Time Of Day, Day Of Week, Day Of Month, Start Time, End Time, Enabled

</td></tr><tr><td>

Eventstreams

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, event throughput level, retention time in days, state, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

Eventstream Source

</td><td>

ID, Name, Status, Type

</td></tr><tr><td>

Eventstream Destination

</td><td>

ID, Name, Status, Type

</td></tr><tr><td>

Environments

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Modified By, State, Library Dependency \(name, library version, library type\), Publish State, Spark Compute \(driver cores, driver memory, executor cores, executor memory\), Dynamic Executor Allocation \(dynamic executor allocation state, max executors, min executors\) Instance Pool \(Type, Id, Name\), Spark Property \(key, value\), Run Time Version, Publish Start Time, Publish End Time, Spark Libraries Publish State, Spark Settings Publish State, Endorsement \(Certified By, Endorsement Badge\)

</td></tr><tr><td>

Database resource types from SQL Server

</td><td>

For a complete list of metadata harvested from SQL server, see the [Microsoft SQL Server collector documentation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/microsoft-sql-server-metadata-collector.md).

</td></tr><tr><td>

Variable library

</td><td>

ID, Name, Description, Created Date, Last Modified Date, Created By, Last Modified By, Active Value Set Name, Variable \(variable type, value, note\)

</td></tr></tbody>
</table>The Microsoft Fabric collector supports the profiling and sampling specific parameters which the SQL Server collector supports and these apply to Warehouses and Lakehouses. When profiling and sampling parameters are enabled, the following additional column information is cataloged:

<table id="table_bjg_xmx_gkc"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Column

</td><td>

-   Average Length \(sample\)
-   Average Value \(sample\)
-   Data Distribution
-   Distinct Values
-   Estimated Distinct Values
-   Estimated Non-null Values
-   Maximum Length \(sample\)
-   Maximum Value \(sample\) sorted numerically or alphabetically \(z-a\)
-   Minimum Length \(sample\)
-   Minimum Value \(sample\) sorted numerically or alphabetically \(a-z\)
-   Non-null Values \(sample\)
-   Sample String Values \(first 5 items in a column\)

</td></tr><tr><td>

Table

</td><td>

-   Row Count
-   Sample Count \(Target sample size\)

</td></tr></tbody>
</table>## Relationship between objects

Catalog pages show relationships between the following data asset types:

|Object|Relationship|
|------|------------|
|Workspace|Warehouses, Lakehouses, Fabric Data Pipelines, Notebooks, Dataflows, Semantic Models, SQL Analytics Endpoints, Eventhouses, Spark Job Definitions, Reports, Dashboards, App, Org App, GraphQL API, Environments, Variable Library|
|App|Workspace|
|Org App|Workspace|
|GraphQL API|Workspace|
|Warehouses|Workspace, Schemas|
|Lakehouses|Workspace, Schemas, Lakehouse Folders, Fabric Delta Lakehouse Table|
|Fabric Data Pipelines|Workspace, Activities which belong to the Pipeline, Refresh Schedule, Variable Library, Data Pipeline Activities, Warehouses, Lakehouses, or SFTP files, Fabric Data Pipelines, Fabric Notebooks, Fabric Dataflows, or Fabric Spark Job Definitions executed by the Activity, Semantic Models refreshed by the Activity, Stored Procedures executed by the Activity|
|Eventhouses|Workspace, KQL Database|
|KQL Databases|Eventhouse|
|Dataflows|Workspace, Logical Tables, Data Sources|
|Notebooks|Workspace, Job Runs, Refresh Schedule, Environments|
|Spark Job Definitions|Workspace, Job Runs, Refresh Schedule, Environments|
|SQL Analytics Endpoints|Workspace, Lakehouse Folders, Lakehouse|
|Lakehouse Folders|Lakehouse, Child Folders, Lakehouse Files|
|Lakehouse Files|Lakehouse Folder|
|Schemas|Lakehouse/Warehouse/Database, Tables, Views|
|Fabric Database Tables|Schema, Columns|
|Fabric Mirrored Database Table|Schema, Columns, Source Database Table|
|Database Columns|Table or View|
|Views|Schema, Columns|
|Reports|Workspace, Dashboard Tile, Report Pages|
|Report Pages|Report|
|Dashboards|Workspace, Dashboard Tiles|
|Dashboard Tiles|Dashboard|
|Semantic Models|Workspace, Logical Tables, Data Sources|
|Data Sources|Semantic Models, Dataflows|
|Dataflow Gen2|Workspace, Logical Tables, Data Sources, Data Destinations, Refresh Schedule|
|Dataflow Gen2 CI/CD|Workspace, Logical Tables, Data Sources, Data Destinations, Refresh Schedule, Job Runs|
|Fabric Lakehouse Delta Tables|Column, Lakehouse, Lakehouse Folder|
|Eventstream|Workspace, Eventstream source, Eventstream destination|
|Eventstream Destination|Published data to lakehouse table, KQL database|
|Environments|Notebooks, Spark Job Definitions, Variable Library, Workspace, Data Pipeline|
|Notebooks|Environments|
|Spark|Job DefinitionsEnvironments|
|Variable Library|Workspace Data Pipeline|

## Lineage and dependencies for Microsoft Fabric

The following lineage information is collected by the Microsoft Fabric collector.

<table id="table_lineage_fabric"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

Database View

</td><td>

The collector identifies the associated column in an upstream view or table:

 -   Where the data is sourced from
-   That sort the rows via ORDER BY
-   That filter the rows via WHERE/HAVING
-   That aggregate the rows via GROUP BY

 **Note:** For views, the collector first tries to parse the view SQL to harvest lineage metadata. If the SQL parser cannot parse the view SQL, the collector catalogs some lineage relationships using the `[dm\_sql\_referencing\_entities](https://learn.microsoft.com/en-us/sql/relational-databases/system-dynamic-management-views/sys-dm-sql-referenced-entities-transact-sql?view=sql-server-ver16#table-returned)` system function, when available. For each row in the referenced entities, if `is_selected` or `is_select_all` is true, the collector catalogs a relationship between the referencing entity and the database column.

</td></tr><tr><td>

Semantic Model

</td><td>

Dataflows and Semantic Models this Semantic Model uses data from.

</td></tr><tr><td>

Dataflow

</td><td>

Other Dataflows this Dataflow uses data from.

</td></tr><tr><td>

Logical Table

</td><td>

Associated tables that the table sources its data from.

 **Note:** The collector uses expressions returned by the Metadata Scan APIs to parse the lineage to the source columns and tables.

</td></tr><tr><td>

Calculated Table

</td><td>

Logical tables and columns from which the calculated table calculates its values.

</td></tr><tr><td>

Logical Column

</td><td>

Associated logical and database columns that the column sources its data from or calculates its values from.

</td></tr><tr><td>

Measure

</td><td>

Associated logical columns that the measure sources its data from.

</td></tr><tr><td>

Dashboard Tile

</td><td>

Associated Semantic Model.

</td></tr><tr><td>

Report

</td><td>

Associated Semantic Model and the Report this Report was published from.

</td></tr><tr><td>

Activity

</td><td>

Establishes lineage between tables or files an Activity copies data to and copies data from. For Copy Activities, see cross-system lineage for supported lineage.

</td></tr><tr><td>

Report Pages

</td><td>

Logical columns and measures from Semantic Model tables that the Report Page uses data from.

</td></tr><tr><td>

Fabric Delta Lakehouse Table

</td><td>

Sourced data from eventstream.

</td></tr><tr><td>

KQL Databases

</td><td>

Sourced data from eventstream.

</td></tr></tbody>
</table>**Supported cross-system lineage**

The following data sources support cross-system lineage with Microsoft Fabric.

**Note:** While other data sources are not formally supported, running the collector for those sources may still enable you to view cross-system lineage between Microsoft Fabric and those sources.

<table id="table_cross_system_lineage"><thead><tr><th>

Object

</th><th>

Supported data sources

</th></tr></thead><tbody><tr><td>

Semantic Models and Dataflows

</td><td>

-   Fabric Lakehouse
-   Fabric Warehouse
-   Oracle
-   Denodo
-   Snowflake
-   SQL Server
-   PostgreSQL
-   Redshift
-   Databricks
-   CSV documents

</td></tr><tr><td>

Fabric Data Pipelines

</td><td>

-   Fabric Delta Lakehouse Tables
-   Fabric Lakehouse Files and Folders
-   Fabric Warehouse Tables
-   SFTP Server Files
-   SQL Server Tables
-   SQL Server Stored Procedures
-   Oracle Tables

</td></tr><tr><td>

Dataflow Gen2 and Dataflow Gen2 CI/CD

</td><td>

-   Fabric Warehouses
-   Fabric Lakehouses

</td></tr></tbody>
</table>**Supported Power Query \(M\) functions and expressions for lineage metadata**

This section captures supported transformations, source expressions, calculated columns, and measure expressions when harvesting lineage metadata.

**Note:** Any table operations or transformations not listed in the following table as supported or unsupported are ignored.

<table id="table_power_query_lineage"><thead><tr><th>

Category

</th><th>

Supported and unsupported objects

</th></tr></thead><tbody><tr><td>

Supported parameterized expressions

</td><td>

The collector parses source expressions that use parameters in place of the following elements: full source value, server or host value, warehouse value, database name, schema name, table name, and SQL expressions that incorporate parameters.

</td></tr><tr><td>

[Supported data functions](https://learn.microsoft.com/en-us/powerquery-m/accessing-data-functions)

</td><td>

Csv.Document, Excel.Workbook, File.Contents, Folder.Contents, Folder.Files, Json.Document, Odbc.DataSource, Odbc.InferOptions, Odbc.Query, Xml.Document, Web.Contents, Web.Headers, Web.BrowserContents, AmazonRedshift.Database, Sql.Database, Sql.Databases, Snowflake.Databases, PostgreSQL.Database, Databricks.Catalogs, Oracle.Database, Denodo.Contents, Databricks.Query, Lakehouse.Contents, Fabric.Warehouse

</td></tr><tr><td>

[Supported table functions](https://learn.microsoft.com/en-us/powerquery-m/table-functions)

</td><td>

Table.AddColumn, Table.AddIndexColumn, Table.RenameColumns, Table.NestedJoin, Table.ExpandTableColumn, Table.SplitColumn, Table.DuplicateColumn, Table.CombineColumns

</td></tr><tr><td>

Unsupported table operations

</td><td>

Table.Pivot, Table.PromoteHeaders, Table.DemoteHeaders, Table.PrefixColumns, Table.TransformColumnNames, Table.Unpivot, Table.UnpivotOtherColumns, Table.AddFuzzyClusterColumn, Table.AddJoinColumn, Table.AggregateTableColumn, Table.Combine, Table.CombineColumnsToRecord, Table.ExpandRecordColumn, Table.Join, Table.Transpose

 **Note:** Contact support if you have expressions that use these unsupported table operations.

</td></tr><tr><td>

Supported dataflow functions

</td><td>

PowerPlatform.Dataflows, PowerBI.Dataflows

</td></tr><tr><td>

[Supported value functions](https://learn.microsoft.com/en-us/powerquery-m/value-functions)

</td><td>

Value.NativeQuery

</td></tr><tr><td>

Supported calculated columns

</td><td>

Lineage from calculated column expressions containing columns with and without table references. Columns or tables with alphanumeric characters, spaces, hyphens, and underscores are supported.

</td></tr><tr><td>

Supported measures

</td><td>

Lineage from measure expressions containing columns or tables with alphanumeric characters, spaces, hyphens, underscores, and surrounding quotes are supported.

</td></tr></tbody>
</table>**Dependencies**

Dependencies between Microsoft Fabric resources are cataloged from the Fabric metadata scan APIs. These relationships are visible in the Lineage Explorer.

## Authentication supported

The collector supports Service principal authentication method.

-   **[Prepare to run the Microsoft Fabric collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/prepare-to-run-microsoft-fabric-collector.md)**  
Set up access and authentication for your Fabric instance before running the collector.
-   **[Create a Microsoft fabric metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/create-microsoft-fabric-metadata-collector.md)**  
Create a collector to import metadata from Microsoft Fabric.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/configure-metadata-collectors-dc.md)

