---
title: Configure Power BI lineage mapping
description: Create a YAML file to map data sources for lineage harvesting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-lineage-mapping.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Prepare to run the PowerBI collector, PowerBI metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Configure Power BI lineage mapping

Create a YAML file to map data sources for lineage harvesting.

## Before you begin

Role required: admin

## About this task

This is an optional task for harvesting lineage information. Create a YAML file and pass it using the Datasource name mapping file option when running the collector.

Set up a YAML file in the following scenarios:

|Scenario|Details|Action|
|--------|-------|------|
|ODBC Connections in Power BI|You have a data source in Power BI that uses an ODBC connection. In these instances, Power BI doesn’t provide the host or database type of the source|In the YAML file, map the DSN to a specific database host and type. If the database name is missing in the Power BI data source, add the defaultDatabaseName option to the data source in the YAML file|
|Multiple Server Name Aliases|You have multiple server names \(aliases\) for the same database instance \(host\) and the database collector uses a different alias than the one defined in the Power BI connection|Use the YAML file to map the database host to user-specified aliases|
|Custom SQL Statements|Custom SQL statements are used in Power BI table source definitions. The Power BI collector currently supports connecting to the following database types to resolve lineage from SQL statements: Snowflake, SQL Server, PostgreSQL, Redshift, Oracle, Databricks, Denodo, BigQuery. Lineage resolution for table sources using SQL statements only supports SQL consisting of a single SELECT statement|Configure databases specified in custom SQL statements by including datasourceKey, host, and secure credentials using environment variables|

**Note:** You can use environment variables in the file for sensitive information such as passwords.

## Procedure

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


**Parent Topic:**[Prepare to run the PowerBI collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.md)

