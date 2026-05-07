---
title: Tableau metadata collector
description: Tableau metadata collector provides read-only access to metadata from a Tableau account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Tableau metadata collector

Tableau metadata collector provides read-only access to metadata from a Tableau account.

The Tableau collector harvests metadata from Tableau objects \(such as workbooks and dashboards\) in the Tableau Online or Tableau Server instances. Use harvested metadata to perform impact analysis and understand how changes to upstream data sources affect Tableau objects.

## Tableau version supported

The collector supports Tableau Cloud and Tableau Server. Supports Tableau API versions 3.10 and above on Tableau Server v2022.1.

## Authentication supported

The Tableau collector supports the following authentication methods:

-   [Personal Access Token](https://help.tableau.com/current/server/en-us/security_personal_access_tokens.htm)

-   [Username and password](https://help.tableau.com/current/blueprint/en-us/bp_authentication_authorization.htm#:~:text=Tableau%20credentials%20are%20made%20up,(SSO)%20via%20OpenID%20Connect.)


## Metadata cataloged

The Tableau collector catalogs the following information:

<table id="table_dyv_5mk_xhc"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Databases

</td><td>

Name, Identifier, Description, Database Connection Type

</td></tr><tr><td>

Database Schemas

</td><td>

Name, Identifier

</td></tr><tr><td>

Database tables

</td><td>

Name, Identifier

</td></tr><tr><td>

Database columns

</td><td>

Name, Identifier

</td></tr><tr><td>

Tableau Databases

</td><td>

Name, Identifier, Connection Type

</td></tr><tr><td>

Tableau Database tables

</td><td>

Name, Identifier, Connection Type

</td></tr><tr><td>

Tableau Database columns

</td><td>

Name, Identifier

</td></tr><tr><td>

Projects

</td><td>

Name, Description

</td></tr><tr><td>

Workbooks

</td><td>

Name, Description, Creator Email, Creator Name, Creator Tableau User, Preview Image, and Workbook URL **Note:** Unpublished workbooks aren’t cataloged because the Tableau REST APIs don’t return unpublished objects.

</td></tr><tr><td>

Dashboards

</td><td>

Name, Creator Email, Creator Name, Creator Tableau User, Preview Image, Dashboard URL, Number of Favorites, and Number of Views**Note:** Unpublished dashboards aren’t cataloged because the Tableau REST APIs don’t return unpublished objects.

</td></tr><tr><td>

Views

</td><td>

Name, Creator Email, Creator Name, Creator Tableau User, Number of Views, Number of Favorites, Preview Image, and View URL**Note:** Unpublished views aren’t cataloged because the Tableau REST APIs don’t return unpublished objects.

</td></tr><tr><td>

Datasource fields

</td><td>

Name, Identifier, Description

</td></tr><tr><td>

Calculated fields

</td><td>

Name, Identifier, Description, Calculation Formula, Category, Role, Type

</td></tr><tr><td>

Group fields

</td><td>

Name, Identifier, Description, Category, Role, Type

</td></tr><tr><td>

Bin fields

</td><td>

Name, Identifier, Description, Category, Role, Type, Bin Size

</td></tr><tr><td>

Column fields

</td><td>

Name, Identifier, Description, Category, Role, Type

</td></tr><tr><td>

Metrics

</td><td>

Name, Identifier, Description, Creator Email, Creator Name, Creator Tableau User, Metric Url

</td></tr><tr><td>

Custom SQL tables

</td><td>

Name, Identifier, Description, SQL Query

</td></tr><tr><td>

Embedded data sources

</td><td>

Name, Identifier, Last refresh date

</td></tr><tr><td>

Published data sources

</td><td>

Name, Identifier, Description, Last refresh date

</td></tr></tbody>
</table>## Relationships between objects

Catalog pages show relationships between the following data asset types:

<table id="table_kvt_2nk_xhc"><thead><tr><th>

Data asset page

</th><th>

Relationship

</th></tr></thead><tbody><tr><td>

Databases

</td><td>

-   Schemas contained within the database
-   Tables contained within the database

</td></tr><tr><td>

Database Schemas

</td><td>

Tables contained within the schema

</td></tr><tr><td>

Database tables

</td><td>

-   Schema containing database table
-   Database containing the database table
-   Views using the database table as a data source
-   Column fields using the database table as a data source

</td></tr><tr><td>

Database columns

</td><td>

-   Tables containing the database columns
-   Column fields referencing the database columns

</td></tr><tr><td>

Tableau Databases

</td><td>

Tableau Tableau Database table contained within the Tableau Database

</td></tr><tr><td>

Tableau Database tables

</td><td>

Tableau Column contained within the Tableau Database table

</td></tr><tr><td>

Tableau Database columns

</td><td>

Tableau Column Field referencing the Tableau Database Column

</td></tr><tr><td>

Projects

</td><td>

-   Views contained within the project
-   Workbooks contained within the project
-   Dashboards contained within the project
-   Subprojects contained within the project
-   Published Data source

</td></tr><tr><td>

Workbooks

</td><td>

-   Projects that contain a workbook
-   Data sources embedded within the workbook
-   Views contained within the workbook
-   Custom SQL Tables embedded within the workbook

</td></tr><tr><td>

Dashboards

</td><td>

-   Fields used by dashboard
-   Custom SQL tables used by dashboard
-   Projects containing dashboard
-   Tables used by dashboard
-   Workbooks containing dashboard
-   Views embedded in dashboard

</td></tr><tr><td>

Views

</td><td>

-   Fields used by view
-   Custom SQL tables used by view
-   Projects containing view
-   Database Tab;es used by view
-   Workbooks containing view
-   Dashboards that embed the view
-   Metrics presenting the view

</td></tr><tr><td>

Datasource fields

</td><td>

-   Views that use the datasource field
-   Dashboards that use the datasource field
-   Data source fields containing the datasource field

</td></tr><tr><td>

Calculated fields

</td><td>

-   Views that use the calculated field
-   Dashboards that use the calculated field
-   Data sources containing the calculated field

</td></tr><tr><td>

Group fields

</td><td>

Data sources containing group field

</td></tr><tr><td>

Bin fields

</td><td>

Data sources containing group field

</td></tr><tr><td>

Column fields

</td><td>

-   Data Source containing the column field
-   Views that use the column field
-   Dashboards that use the column field

</td></tr><tr><td>

Custom SQL tables

</td><td>

-   Views using Custom SQL table
-   Dashboards using Custom SQL table
-   Workbooks using Custom SQL table

</td></tr><tr><td>

Embedded data sources

</td><td>

-   Fields contained within the embedded data source
-   Workbook containing embedded data source

</td></tr><tr><td>

Published data sources

</td><td>

Fields contained within the published data source

</td></tr></tbody>
</table>## Lineage for Tableau

Collected lineage information:

|Object|Lineage available|
|------|-----------------|
|Database columns and tables|Fields that use database columns and tables|
|Projects|Databases, Database schemas, Database Tables, Database Columns, Workbooks, Views, Dashboards, custom SQL tables, and Data sources that projects contain|
|Dashboards|Fields and tables that dashboards source their data from|
|Views|Fields and tables that views source their data from|
|Fields|Columns, tables, and other fields that a field uses its data from|
|Tableau Database tables|Tableau Databases containing the Tableau Database table|
|Tableau Database columns|Fields that reference the Tableau Database column, Tableau Database tables containing the Tableau Database column|
|Published data sources|Embedded data sources that were derived from published data source|
|Embedded data sources|Database tables and Database columns that the Embedded data source uses data from.|
|Custom SQL Tables|Database tables and Database columns that the Custom SQL Table uses data from. Note: Lineage isn’t created between Custom SQL Tables and columns or tables that aren’t available in the API.|

**Note:** Cross-system lineage isn’t supported for ODBC connections or when columns or tables are unavailable in the API.

Supported data sources for cross-system lineage:

-   Postgresql
-   Snowflake
-   BigQuery
-   Redshift

-   **[Prepare to run the Tableau collector](../task/prepare-to-run-tableau-collector.md#)**  
Set up API access, authentication, and permissions before running the collector.
-   **[Create a Tableau metadata collector](../task/create-tableau-metadata-collector.md)**  
Create a collector to import metadata from Tableau.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

