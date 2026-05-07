---
title: PowerBI metadata collector
description: The PowerBI metadata collector provides read-only access to metadata from a PowerBI account.Set up Azure application registration, authentication, and permissions before running the collector.Register an application in Azure and create client credentials for Power BI collector authentication.Set up service principal authentication to enable Power BI metadata collection.Set up API permissions for username and password authentication to enable Power BI metadata collection.Enable metadata scanning to access detailed data source information including tables and columns.Retrieve the tenant ID from the Power BI application.Enable report image harvesting to collect preview images from Power BI reports.Create a YAML file to map data sources for lineage harvesting.Create a collector to import metadata from PowerBI.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 19
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

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

## Prepare to run the PowerBI collector

Set up Azure application registration, authentication, and permissions before running the collector.

### Before you begin

Role required: admin

**Important:** A Power BI Administrator is needed to enable settings in the Power BI Admin Portal.

### About this task

The collector uses Azure application registration and supports two authentication methods: service principal or username and password. You must register an application, configure authentication, enable metadata scanning, and retrieve the tenant ID. Optionally, configure report image harvesting and lineage mapping.

### Procedure

1.  Register an application in Azure and create client credentials.

    See [Register Power BI application](powerbi-metadata-collector.md#).

2.  Configure authentication based on your preferred method.

    -   For service principal authentication, see [Configure Power BI service principal authentication](powerbi-metadata-collector.md#).

    -   For username and password authentication, see [Configure Power BI username and password authentication](powerbi-metadata-collector.md#).

3.  Enable metadata scanning to access detailed data source information.

    See [Configure Power BI metadata scanning](powerbi-metadata-collector.md#).

4.  Get the Power BI tenant ID.

    See [Get Power BI tenant ID](powerbi-metadata-collector.md#).

5.  Configure report image harvesting to collect preview images from Power BI reports.

    See [Configure Power BI report image harvesting](powerbi-metadata-collector.md#).

6.  Configure lineage mapping for ODBC connections, server aliases, or custom SQL statements.

    See [Configure Power BI lineage mapping](powerbi-metadata-collector.md#) .


### Register Power BI application

Register an application in Azure and create client credentials for Power BI collector authentication.

#### Before you begin

Role required: admin

You must have permissions to register applications in Azure Active Directory.

#### About this task

Register an application in Azure to obtain the client ID and client secret needed for Power BI collector authentication.

#### Procedure

1.  Register a new application in Azure.

    1.  Navigate to the [Azure Portal](https://portal.azure.com).

    2.  Select **App Registrations** from Azure services.

    3.  Select **New Registration**.

    4.  Enter the registration information.

        -   Application Name: DataDotWorldPowerBIApplication
        -   Supported account types: Accounts in this organizational directory only
    5.  Select **Register** to complete the registration.

2.  Create a client secret.

    1.  On the application page, select **Certificates and Secrets**.

    2.  Select **New client secret**.

    3.  Add a description for the secret.

    4.  Select the desired expiration date.

    5.  Select **Add**.

    6.  Copy the secret value.

        Save this value securely. You will use it when configuring the Power BI collector.

3.  Get the client ID.

    1.  Select the **Overview** tab in the left sidebar of the application page.

    2.  Copy the Client ID from the Essentials section.

        Save this value. You will use it when configuring the Power BI collector.


### Configure Power BI service principal authentication

Set up service principal authentication to enable Power BI metadata collection.

#### Before you begin

Role required: admin

You must be a Power BI administrator to enable service principal settings.

**Important:** When running under a service principal, there must be no Power BI admin-consent-required permissions set on your app. For more information, see the [Microsoft documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-premium-service-principal).

#### About this task

When using service principal authentication, the collector harvests all objects except personal workspaces, user workspaces, and report pages. To harvest all apps and workspaces in the tenant, enable Catalog all workspaces and apps in the tenant. To include personal and user workspaces, enable Catalog contents of user's My Workspace.

**Note:** To harvest report pages, grant the service principal access to each workspace. The admin API doesn’t have an endpoint for report pages.

#### Procedure

1.  Sign in to Power BI using a Power BI Admin account.

2.  Navigate to **Settings** &gt; **Admin Portal**.

3.  Enable service principal API access.

    1.  Under **Developer settings**, locate **Service principals can use Fabric APIs**.

    2.  Enable the setting.

    3.  Select whether the setting applies to the entire organization or specific security groups.

        If using specific security groups, confirm that the group includes the service principal.

    4.  Select **Apply** to save the changes.

4.  Add the service principal to workspaces for dataflow and report page access.

    Dataflows require the service principal to have at least Contributor access to the workspace. For report pages, the service principal also needs workspace access because the admin API doesn’t provide an endpoint for report pages.

    1.  Open the workspace.

    2.  Select **Manage access**.

    3.  Search for the service principal or the security group the service principal belongs to.

    4.  Select the appropriate access level.

        If dataflows are used, select at least Contributor access. Otherwise, select Viewer.

    5.  Select **Add**.


### Configure Power BI username and password authentication

Set up API permissions for username and password authentication to enable Power BI metadata collection.

#### Before you begin

Role required: admin

You must have permissions to configure API permissions in Azure Active Directory.

**Note:** Only administrators of the tenant can grant admin consent.

#### About this task

When using user authentication, the collector harvests all objects except personal workspaces, user workspaces, and report pages. To harvest all apps and workspaces in the tenant, enable Catalog all workspaces and apps in tenant. To include personal and user workspaces, enable Catalog contents of user's My Workspace.

To harvest report pages, grant the user access to each workspace. The admin API doesn’t have an endpoint for report pages.

**Note:** Catalog all workspaces and apps in the tenant requires the user to have Microsoft 365 Global Administrator or Power BI Service Administrator rights for metadata scanning. For details, see the [Power BI documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-admin-metadata-scanning).

#### Procedure

1.  Navigate to the Azure Portal and open the application registration.

2.  Select **API Permissions**.

3.  Add Microsoft Graph permissions.

    1.  Select **Add a permission**.

    2.  Search for and select **Microsoft Graph**.

    3.  Add the following permissions.

        -   Application permission: Application.Read.All
        -   Delegated permission: User.Read \(assigned by default\)
4.  Add Power BI service permissions.

    1.  Select **Add a permission**.

    2.  Search for and select **Power BI service**.

    3.  Select **Delegated permissions**.

    4.  Add the following permissions.

        -   App.Read.All
        -   Dashboard.Read.All
        -   Dataflow.Read.All
        -   Dataset.Read.All
        -   Report.Read.All
        -   Tenant.Read.All
        -   Workspace.Read.All
5.  Select the **Grant admin consent** button located next to the **Add a permission** button.

    This permission enables the collector to run without asking you for permission on every run.


### Configure Power BI metadata scanning

Enable metadata scanning to access detailed data source information including tables and columns.

#### Before you begin

Role required: admin

You must be a Power BI administrator to enable metadata scanning settings.

#### About this task

[Metadata scanning](https://learn.microsoft.com/en-us/fabric/governance/metadata-scanning-overview) provides access to detailed data source information, such as tables and columns, through Power BI read-only admin APIs. The collector uses the Power BI Scanner APIs to establish lineage to source tables and columns. Review the [limitations to the scanner APIs](https://learn.microsoft.com/en-us/power-bi/enterprise/service-admin-metadata-scanning) before configuring the collector.

#### Procedure

1.  Enable metadata scanning based on your authentication method.

    -   For service principal authentication:

        1.  Follow the [Power BI documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-premium-service-principal) to enable service principal authentication for Power BI read-only APIs
        2.  Enable the following enhanced tenant settings for metadata scanning:
            -   Enhance admin APIs responses with detailed metadata
            -   Enhance admin APIs responses with DAX and mashup expressions
    -   For username and password authentication, enable the following enhanced tenant settings for metadata scanning:

        **Important:** The user must have administrator rights \(Microsoft 365 Global Administrator or Power BI Service Administrator\) to use metadata scanning. For details, see the [Power BI documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-admin-metadata-scanning).

        -   Enhance admin APIs responses with detailed metadata
        -   Enhance admin APIs responses with DAX and mashup expressions

### Get Power BI tenant ID

Retrieve the tenant ID from the Power BI application.

#### Before you begin

Role required: admin

#### About this task

The tenant ID is required when configuring the Power BI collector. Retrieve this value from the Power BI application.

#### Procedure

1.  In the Power BI application, select the question mark icon.

2.  Select **About Power BI**.

3.  Copy the tenant ID from the end of the Tenant URL.

    Save this value. You will use it when configuring the Power BI collector.


### Configure Power BI report image harvesting

Enable report image harvesting to collect preview images from Power BI reports.

#### Before you begin

Role required: admin

**Note:** Report image harvesting isn’t supported for Power BI Apps.

#### About this task

Enable report image harvesting to collect preview images from Power BI reports for display in the Data Catalog.

#### Procedure

1.  Enable the export setting in the Power BI Admin Portal.

    1.  Sign in to Power BI using a Power BI Admin account.

    2.  Navigate to **Settings** &gt; **Admin Portal**.

    3.  Locate and enable the **Export reports as image files** setting from the [Admin settings](https://learn.microsoft.com/en-us/power-bi/developer/embedded/export-to#using-the-api).

2.  Verify workspace capacity.

    Confirm that the reports to be exported are located in a workspace with Premium, Embedded, or Fabric capacity. For details, see the [Power BI documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-premium-what-is).


### Configure Power BI lineage mapping

Create a YAML file to map data sources for lineage harvesting.

#### Before you begin

Role required: admin

#### About this task

This is an optional task for harvesting lineage information. Create a YAML file and pass it using the Datasource name mapping file option when running the collector.

Set up a YAML file in the following scenarios:

|Scenario|Details|Action|
|--------|-------|------|
|ODBC Connections in Power BI|You have a data source in Power BI that uses an ODBC connection. In these instances, Power BI doesn’t provide the host or database type of the source|In the YAML file, map the DSN to a specific database host and type. If the database name is missing in the Power BI data source, add the defaultDatabaseName option to the data source in the YAML file|
|Multiple Server Name Aliases|You have multiple server names \(aliases\) for the same database instance \(host\) and the database collector uses a different alias than the one defined in the Power BI connection|Use the YAML file to map the database host to user-specified aliases|
|Custom SQL Statements|Custom SQL statements are used in Power BI table source definitions. The Power BI collector currently supports connecting to the following database types to resolve lineage from SQL statements: Snowflake, SQL Server, PostgreSQL, Redshift, Oracle, Databricks, Denodo, BigQuery. Lineage resolution for table sources using SQL statements only supports SQL consisting of a single SELECT statement|Configure databases specified in custom SQL statements by including datasourceKey, host, and secure credentials using environment variables|

**Note:** You can use environment variables in the file for sensitive information such as passwords.

#### Procedure

1.  Create a YAML file named datasources.yml.

2.  Configure the YAML file based on your scenario.

    -   For multiple server name aliases:

        Add the following to map a host alias:

        ```
        datasources:
         - datasourceKey: "<host or data source key in Power BI source>"
          host: <my-datasource-host>
        ```

        For example, if your Power BI table source is:

        ```
        let Source = Snowflake.Database("host-alias.snowflakecomputing.com", "KOS_TEST"),
        PowerBiTest_Test_Table = Source{[Schema="POWERBI_TEST",Item="TEST_TABLE"]}[Data]
        in PowerBiTest_Test_Table
        ```

        Then the datasourceKey will be host-alias.snowflakecomputing.com. Your datasources.yml file will look like:

        ```
        datasources:
        - datasourceKey: host-alias.snowflakecomputing.com
        host: host-actual.snowflakecomputing.com
        ```

    -   For custom SQL statements:

        Add the following for databases specified in custom SQL statements. Environment variables are supported:

        ```
        datasources:
          - datasourceKey: "<host or data source key in Power BI source>"
          OR
         - name: <data source name>
         host: <my-datasource-host>
         databaseUsername: <username> # recommend setting up env variable
         databasePassword: <password> # recommend setting up env variable
        ```

        Use the following option to specify which databases a datasource configuration applies to. If not provided, it’s assumed that the datasource settings apply to all databases on the given host:

        ```
        applicableDatabases:
          - <database_name>
        ```

        For example:

        ```
        datasources:
        - datasourceKey: "example.cpcnqsn422gx.us-east-1.rds.amazonaws.com, 1433"
         host: example.cpcnqsn422gx.us-east-1.rds.amazonaws.com
         databaseUsername: ${DB_USERNAME}
         databasePassword: ${DB_PASSWORD}
         applicableDatabases:
         - 8bank_database
        ```

    -   For ODBC connections:

        Map the DSN to a specific database host and type. For ODBC connections, list data sources with their corresponding host and database type. If ODBC connections use Odbc.Query, specify the user name and password. If ODBC connections specify the database name, include defaultDatabaseName:

        ```
        datasources:
        - name: "Name-for-datasource"
        host: <my-datasource-host>
        databaseType: <type-of-database>
        databaseUsername: <username> # optional
        databasePassword: <password> # optional
        defaultDatabaseName: <database name> # optional
        ```

        The list of possible databaseTypes are: postgres, redshift, bigquery, oracle, mysql, netezza, snowflake, sqlanywhere, sqlserver, databricks, denodo. Types aren’t case-sensitive but should be a single word with no spaces.

        For example:

        ```
        datasources:
        - name: "SQL Server DSN Production"
        databaseType: sqlserver
        host: 8bank-sqlserver.cpetgx.us-east-1.rds.amazonaws.com
        ```

3.  Add database-specific configuration options if necessary.

    JDBC properties options:

<table id="table_jdbc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

jdbcProperties

</td><td>

Multiple JDBC properties can be specified using a YAML list. The expected format is jdbcProperties: key=value For example: jdbcProperties: encrypt=true

 For multiple values:

 ```
jdbcProperties:
- encrypt=true
- readOnly=true
```

</td></tr></tbody>
</table>    Snowflake database credentials options:

    |Option|Description|
    |------|-----------|
    |databaseUsername: $\{DB\_USERNAME\}|Required if custom SQL queries are used in Power BI database sources|
    |databasePassword: $\{DB\_PASSWORD\}|Required if SQL queries are used and if a private key isn’t used for authentication to Snowflake|
    |snowflakePrivateKeyFile: privateKeyFile|Required if SQL queries are used and if a private key is used for authentication to Snowflake|
    |snowflakePrivateKeyFilePassword: $\{privateKeyFilePassword\}|Required if SQL queries are used and if a private key is used for authentication to Snowflake|
    |snowflakeRole: role|Required if SQL queries are used|
    |snowflakeWarehouse: warehouse|Use to override warehouses used in Power BI expressions in the database connection|

    Databricks database credentials options:

    |Option|Description|
    |------|-----------|
    |databricksHttpPath|Required if the source database is Databricks|

    Oracle Autonomous Database options:

<table id="table_oracle"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

oracleAutonomousDbConnectionString

</td><td>

Required if the source is an Oracle Autonomous Database. The connection string should be in the format:```
jdbc:oracle:thin:<host>:<port>/<service_name>, 
jdbc:oracle:thin:@(address=(protocol=tcps)(port=<port>)(host:<host>))
(connect_data=(service_name=<service_name>))
(security=(ssl_server_dn_match=yes)), 
or jdbc:oracle:thin:@alias_name?TNS_ADMIN=/path/to/wallet

```

</td></tr></tbody>
</table>    BigQuery options:

    |Option|Description|
    |------|-----------|
    |project|Required if the source is a BigQuery table|
    |bigQueryCredentialJsonString|Required for supplying BigQuery credentials|

    Example for BigQuery database:

    ```
    datasources:
     - project: "project-name"
    databaseType: bigquery
    bigQueryCredentialJsonString: '{"key": "value","key": "value"}'
    ```

4.  Save the datasources.yml file.

5.  Pass the YAML file to the collector using the --datasource-mapping-file parameter when running the collector.


## Create a PowerBI metadata collector

Create a collector to import metadata from PowerBI.

### Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the PowerBI collector](powerbi-metadata-collector.md#).
-   Role required: connection-admin

### Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **PowerBI**.

5.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field cannot be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

6.  Configure the authentication options.

    |Field|Description|
    |-----|-----------|
    |Authenticate using Azure username and password|Azure Active Directory username and password. Set the Azure Tenant ID if you want to specify the Azure tenant ID while using the user name and password authentication.|
    |Authenticate using Azure Service principal|Azure Active Directory application tenant ID for Power BI app. To find the tenant ID, select the question mark in the Power BI app and then choose About Power BI. The tenant ID is found at the end of the Tenant URL.|

7.  Configure the client ID and client secret details.

    |Field|Description|
    |-----|-----------|
    |Microsoft Entra client ID|Application client ID for the PowerBI app.|
    |Microsoft Entra client secret|Application client secret for the PowerBI app.|

8.  Configure the workspace scope and filters options.

<table id="table_qpw_5xc_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable Lineage collection

</td><td>

Option to skip harvesting lineage metadata from Power BI source expressions.

</td></tr><tr><td>

Catalog contents of user's My Workspace

</td><td>

Option to catalog the contents of a user's My Workspace in Power BI. Default: Skip the user's workspace.

</td></tr><tr><td>

Catalog all workspaces and apps in tenant

</td><td>

Option to catalog all workspaces and apps in a tenant, rather than only the workspaces and apps the credentials have explicit access to. Admin privileges are required for the credentials used.

</td></tr><tr><td>

Include Power BI workspace\(s\)

</td><td>

Workspaces to collect. Enter the exact workspace name or a regular expression to match. **Note:** If a workspace name includes special characters \[. , + , \* , ? , ^ , $ , \( , \) , \[ , \] , \{ , \} , \| , \\\], escape each special character with a backslash \(\\\). For example, enter Workspace \\\(Dev\\\) for Workspace \(Dev\).

</td></tr><tr><td>

Exclude Power BI Workspaces

</td><td>

Power BI workspaces and their contents to exclude from cataloging. Enter the exact workspace name or a regular expression to match. If both Include Workspaces and Exclude Workspaces are configured, Include Workspaces takes precedence. **Note:** If a workspace name includes special characters \[. , + , \* , ? , ^ , $ , \( , \) , \[ , \] , \{ , \} , \| , \\\], escape each special character with a backslash \(\\\). For example, enter Workspace \\\(Dev\\\) for Workspace \(Dev\).

</td></tr></tbody>
</table>9.  Configure the connection and reliability options.

<table id="table_yhb_plp_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum Power BI Expression Length

</td><td>

Maximum number of characters in a Power BI expression that is parsed for lineage metadata. Expressions longer than this value are skipped. Default: 32000

</td></tr><tr><td>

Datasource Name Mapping File

</td><td>

File that maps ODBC source details configured in the [datasources.yml](powerbi-metadata-collector.md#)file. Upload the file if you have configured ODBC source details.

</td></tr><tr><td>

Catalog report preview images

</td><td>

Option to catalog preview images. Default: false

</td></tr><tr><td>

Disable max requests wait

</td><td>

Option to disable waiting for the Power BI API to reset throttling limits \(error code 429\). When not selected, the collector retries every 5 minutes for up to an hour. When selected, the Max retries and Retry delay settings are used instead.

</td></tr><tr><td>

Max retries

</td><td>

Number of times the system retries a failed API call. Default: 5

</td></tr><tr><td>

Retry delay

</td><td>

Number of seconds to wait between retry attempts for a failed API call. Default: 2 seconds

</td></tr></tbody>
</table>10. Select **Save**.


### Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

### What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](../task/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](../task/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](../task/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](manage-data-catalog.md).

