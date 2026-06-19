---
title: PowerBI metadata collector
description: The PowerBI metadata collector provides read-only access to metadata from a PowerBI account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/powerbi-metadata-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# PowerBI metadata collector

The PowerBI metadata collector provides read-only access to metadata from a PowerBI account.

[Power BI](https://learn.microsoft.com/en-us/power-bi/fundamentals/power-bi-overview) is a collection of software services, apps, and connectors that work together to transform unrelated data sources into coherent, visually immersive, and interactive insights. Data sources can include Excel spreadsheets, cloud-based data warehouses, or on-premises hybrid data warehouses. Power BI enables you to connect to data sources, visualize and discover important information, and share insights across the organization.

The Power BI collector harvests metadata from Power BI service workspaces. Use harvested metadata to discover reports and dashboards across workspaces and perform impact analysis to understand how changes to upstream data sources affect Power BI reports.

## Version supported

The collector supports Power BI Cloud API v 1.0.

## Authentication supported

Power BI supports two authentication methods:

-   Service principal
-   User and password

The collector harvests metadata for all Power BI apps and workspaces the authenticated account has access to.

## Metadata cataloged

The Power BI collector catalogs the following information:

|Object|Information collected|
|------|---------------------|
|Workspaces|Title, Description|
|Apps|Title, Description|
|Power BI measures|Title, Description, Is hidden, Expression|
|Reports|Title, Reports type, External URL, Embed URL, Preview Image \(not supported for paginated report types\), Created date, Last modified, Created by, Last modified by, Descriptions|
|Report pages|Title Note: Report pages within Apps can’t be cataloged when using Service Principal authentication due to restrictions in the Power BI APIs.|
|Dashboards|Title, External URL, Embed URL|
|Dashboard tiles|Title, Embed URL|
|Data Sources|Title, Data source type, Connection Details \(kind and path\)|
|Semantic model|Title, External URL, Description, Created date, Created by, Refresh Schedule|
|Dataflows|Title, Last modified, Description, Created by, Refresh Schedule|
|Power BI tables \(Semantic model and Dataflows\)|Title, Is hidden, Is Entered Data, Description, Source expression|
|Power BI calculated table|Title, Is hidden, Is Entered Data, Description, Source expression|
|Power BI columns|Title, Descriptions, Data type, Column type, Is hidden, Expression|
|Tabular file|File path, File name|
|File directory|Directory path|
|Database|Title, Type, Identifier, Server, Port|
|Database schema|Title|
|Database table|Title|
|Database column|Title|
|Table|Title, Description|
|Column|Title, Type|
|Calculation group|Title, Description|
|Calculation item|Title, Description, Expression|

## Relationships between objects

Catalog pages show relationships between the following data asset types:

<table id="table_fbw_d4c_l3c"><thead><tr><th>

Data asset page

</th><th>

Relationship

</th></tr></thead><tbody><tr><td>

App

</td><td>

Report, Dashboard, Workspace

</td></tr><tr><td>

Power BI Column

</td><td>

Power BI Table

</td></tr><tr><td>

Data source

</td><td>

Semantic model, Dataflow, Tabular Data source \(Database, Tabular File\)

</td></tr><tr><td>

Tile

</td><td>

Dashboard, Report, Semantic model

</td></tr><tr><td>

Dashboard

</td><td>

Tile, Workspace

</td></tr><tr><td>

Dashboard Tile

</td><td>

Associated Semantic model

</td></tr><tr><td>

Semantic model

</td><td>

Dashboard Tile, Report

</td></tr><tr><td>

Report

</td><td>

Tile, Workspace, Report pages \(not applicable for paginated report types\), Semantic model \(not applicable for paginated report types\), Report **Note:** In Power BI, app reports and their associated workspace reports are two separate reports with unique report IDs. The collector catalogs the relationship between them.

</td></tr><tr><td>

Report Pages

</td><td>

Report \(not applicable for paginated report types\)

</td></tr><tr><td>

Semantic model

</td><td>

Tile, Workspace, Report, Table, Data source, Semantic model, Dataflow

</td></tr><tr><td>

Workspace

</td><td>

Report, Semantic model, Dataflow, Dashboard, App

</td></tr><tr><td>

Dataflow

</td><td>

Workspace, Table, Data source, Dataflow

</td></tr><tr><td>

Power BI Table

</td><td>

Semantic model, Dataflow, Power BI Column, Power BI Measure

</td></tr><tr><td>

Power BI Measure

</td><td>

Power BI Table

</td></tr><tr><td>

Tabular Data source \(Database, Tabular File\)

</td><td>

Data source

</td></tr><tr><td>

Calculation Group

</td><td>

Power BI Table

</td></tr><tr><td>

Calculation Item

</td><td>

Calculation Group

</td></tr></tbody>
</table>## Lineage for PowerBI

The following lineage information is collected by the Power BI collector. The collector uses the [Power BI Scanner APIs](https://docs.data.world/en/197965-preparing-to-run-the-power-bi-gov-collector.html#UUID-54824f09-f93b-9459-1077-457716965021_section-idm682803229937714) to establish lineage to source tables and columns. Be sure to familiarize yourself with the [limitations to the scanner APIs](https://learn.microsoft.com/en-us/fabric/governance/metadata-scanning-run#considerations-and-limitations)

<table id="table_igt_l4c_l3c"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

Dashboard Tile

</td><td>

Associated Semantic model

</td></tr><tr><td>

Semantic model

</td><td>

Associated Dataflow, Semantic model

</td></tr><tr><td>

Dataflow

</td><td>

Dataflow

</td></tr><tr><td>

Power BI Column

</td><td>

Associated columns that the column sources its data from or calculates its values from. **Note:** Lineage can be harvested from Power BI expressions that use parameters in place of server, schema, table, or database names. Table-level and column-level lineage and catalog relationships aren’t available between tables or columns and reports through the Power BI API.

</td></tr><tr><td>

Power BI table

</td><td>

Associated tables that the table sources its data from Note: **Note:** The collector uses Power BI expressions returned by the APIs to parse the lineage to the source columns/tables.

</td></tr><tr><td>

Power BI calculated table

</td><td>

Power BI tables and columns from which the calculated table derives its values.

</td></tr><tr><td>

Power BI Measure

</td><td>

Associated columns that the measure sources it data from

</td></tr></tbody>
</table>The following table lists supported and unsupported table operations and transformations. This includes source expressions, calculated columns, and measure expressions used in lineage metadata harvesting. Unlisted operations are not harvested.

|Category|Category|
|--------|--------|
|Supported Parameterized Expressions|The collector parses source expressions that use parameters in place of the following values: full source, server or host, warehouse, database name, schema name, table name, and SQL expressions.|
|[Supported data functions](https://learn.microsoft.com/en-us/powerquery-m/accessing-data-functions)|Csv.Document, Excel.Workbook, File.Contents, Folder.Contents, Folder.Files, Json.Document, Odbc.DataSource, Odbc.InferOptions, Odbc.Query, Xml.Document, Web.Contents, Web.Headers, Web.BrowserContents, AmazonRedshift.Database, Sql.Database, Sql.Databases, Snowflake.Databases, PostgreSQL.Database, Databricks.Catalogs, Oracle.Database, Denodo.Contents, Databricks.Query, DatabricksMultiCloud.Catalogs, AnalysisServices.Database, GoogleBigQuery.Database|
|[Supported table functions](https://learn.microsoft.com/en-us/powerquery-m/table-functions)|Table.AddColumn, Table.AddIndexColumn, Table.RenameColumns, Table.NestedJoin, Table.ExpandTableColumn, Table.SplitColumn, Table.DuplicateColumn, Table.CombineColumns|
|Unsupported table operations|Table.Pivot, Table.PromoteHeaders, Table.DemoteHeaders, Table.PrefixColumns, Table.TransformColumnNames, Table.Unpivot, Table.UnpivotOtherColumns, Table.AddFuzzyClusterColumn, Table.AddJoinColumn, Table.AggregateTableColumn, Table.Combine, Table.CombineColumnsToRecord, Table.ExpandRecordColumn, Table.Join, Table.Transpose|
|Supported dataflow functions|PowerPlatform.Dataflows, PowerBI.Dataflows|
|[Supported value functions](https://learn.microsoft.com/en-us/powerquery-m/value-functions)|Value.NativeQuery|
|Supported calculated columns|Lineage from calculated column expressions containing columns with and without table references, Columns or tables with alphanumeric characters, Spaces, Hyphens, and Underscore are supported|
|Supported measures|Lineage from measure expressions containing columns or tables with alphanumeric characters, Spaces, Hyphens, Underscore, Surrounding quotes are supported|

-   **[Prepare to run the PowerBI collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.md)**  
Set up Azure application registration, authentication, and permissions before running the collector.
-   **[Create a PowerBI metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/create-powerbi-metadata-collector.md)**  
Create a collector to import metadata from PowerBI.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-metadata-collectors-dc.md)

