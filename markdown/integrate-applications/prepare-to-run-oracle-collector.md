---
title: Prepare to run the Oracle collector
description: Set up database user permissions and configure advanced features before running the collector.Create a dedicated Oracle user and grant permissions for metadata harvesting.Grant AWR view permissions to enable historical lineage extraction from CREATE TABLE statements.Configure database links and gather connection information for cross-server lineage harvesting.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Oracle metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Oracle collector

Set up database user permissions and configure advanced features before running the collector.

## Before you begin

Role required: admin

## About this task

The collector requires a dedicated Oracle database user with SELECT and EXECUTE permissions. You must create the database user and grant appropriate permissions to catalog schemas, tables, views, procedures, functions, and packages.

## Procedure

1.  Create Oracle user and grant permissions.

    See [Set up user permissions](prepare-to-run-oracle-collector.md#).

2.  Prepare to harvest cross-server lineage.

    See [Set up AWR permissions for lineage extraction](prepare-to-run-oracle-collector.md#).

3.  Prepare to harvest from autonomous databases.

    See [Prepare to harvest cross-server lineage](prepare-to-run-oracle-collector.md#).


**Parent Topic:**[Oracle metadata collector](../concept/oracle-metadata-collector.md)

## Set up user permissions

Create a dedicated Oracle user and grant permissions for metadata harvesting.

### Before you begin

Role required: admin

### About this task

To harvest data from an Oracle database, create a dedicated user with the required permissions. Grant this user SELECT and EXECUTE privileges on the necessary schemas, tables, views, procedures, functions, and packages. Alternatively, you can grant broader access using DBA views or catalog roles to ensure full data harvesting capabilities.

These steps configure a user with the permissions required for efficient data harvesting.

### Procedure

1.  Create a user.

    ```
    CREATE USER ddw_user IDENTIFIED BY <password>;
    ```

    Replace &lt;password&gt; with a secure password.

2.  Grant SELECT and EXECUTE permissions to the user.

    **Primary approach:** Grant permissions on specific objects.

    ```
    GRANT CREATE SESSION, SELECT_CATALOG_ROLE TO ddw_user;
                            
                            -- Update <schemaName> and <tableName> for each schema, table, or view you want to harvest.
                            GRANT SELECT ON "<schemaName>"."<tableName>" TO ddw_user;
                            
                            -- Update <schemaName> and <procedureName> for each schema and procedure, function, or package you want to harvest.
                            GRANT EXECUTE ON "<schemaName>"."<procedureName>" TO ddw_user;
    ```

    -   In the SELECT command, update &lt;schemaName&gt; and &lt;tableName&gt; for each schema, table, or view you want to harvest.
    -   In the EXECUTE command, update &lt;schemaName&gt; and &lt;procedureName&gt; for each schema and procedure, function, or package you want to harvest.
    **Alternate approach for EXECUTE permissions:** Grant SELECT permission on the following DBA views, or give the user the SELECT\_CATALOG\_ROLE role, which grants SELECT privileges on all DBA static data dictionary views:

    -   DBA\_PROCEDURES
    -   DBA\_ARGUMENTS
    -   DBA\_SOURCE
    -   DBA\_DEPENDENCIES
    -   DBA\_OBJECTS
    -   DBA\_SYNONYMS
    **Alternative approach for SELECT permissions:** Grant SELECT permission on the following DBA views, or give the user the SELECT\_CATALOG\_ROLE role, which grants SELECT permission on all DBA static data dictionary views:

    **Important:** If SELECT privileges aren’t granted for the tables, the collector is unable to catalog column statistics.

    -   DBA\_VIEWS
    -   DBA\_MVIEWS
    -   DBA\_OBJECTS
    -   DBA\_CONS\_COLUMNS
    -   DBA\_CONSTRAINTS
    -   DBA\_COL\_COMMENTS
    -   DBA\_TAB\_COMMENTS
    -   DBA\_SOURCE
    -   DBA\_DEPENDENCIES
    -   DBA\_SYNONYMS
    **Grant comprehensive permissions:** If you want to grant the user permission to catalog any object in any schema, use the following commands:

    ```
    GRANT SELECT ANY TABLE TO ddw_user;
                            GRANT EXECUTE ANY PROCEDURE TO ddw_user;
    ```


## Set up AWR permissions for lineage extraction

Grant AWR view permissions to enable historical lineage extraction from CREATE TABLE statements.

### Before you begin

Role required: admin

License required: Oracle Diagnostics Pack license.

### About this task

The Oracle collector queries AWR \(Automatic Workload Repository\) views to extract lineage from historical CREATE TABLE statements. Grant SELECT permissions on DBA\_HIST\_\* views to enable this capability.

### Procedure

1.  Grant AWR view permissions.

    ```
    GRANT SELECT ON DBA_HIST_SQLTEXT TO ddw_user;
               GRANT SELECT ON DBA_HIST_SQLSTAT TO ddw_user;
               GRANT SELECT ON DBA_HIST_SNAPSHOT TO ddw_user;
    ```


## Prepare to harvest cross-server lineage

Configure database links and gather connection information for cross-server lineage harvesting.

### Before you begin

Role required: admin

### About this task

If your Oracle database includes objects with SQL definitions that reference another server, follow these steps to capture cross-server lineage. In Oracle, these references are called database links \(DB links\). To resolve lineage for SQL that uses DB links, the collector requires the host and port information for each linked database.

### Procedure

1.  Find all database links.

    Use ALL\_DB\_LINKS or DBA\_DB\_LINKS to find the full list of DB links.

    See the [Oracle database links documentation](https://docs.oracle.com/en/database/oracle/oracle-database/19/refrn/ALL_DB_LINKS.html) for details.

2.  Gather connection information for each DB link.

    For each DB link entry, work with your Oracle Admin to find:

    -   Hostname
    -   Database name
    -   Port information
3.  Record the information for collector configuration.

    This information is passed to the collector using the Linked host parameter.


