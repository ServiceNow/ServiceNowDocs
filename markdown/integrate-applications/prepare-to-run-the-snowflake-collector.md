---
title: Prepare to run the Snowflake collector
description: Set up authentication and grant role permissions to enable Snowflake metadata collection.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Snowflake metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Snowflake collector

Set up authentication and grant role permissions to enable Snowflake metadata collection.

## Before you begin

Role required: ACCOUNTADMIN

You must have an ACCOUNTADMIN role in Snowflake to grant permissions.

## About this task

The collector supports username and key-pair authentication. For details, see the [Snowflake documentation](https://docs.snowflake.com/en/user-guide/key-pair-auth.html).

Snowflake determines authorization based on roles. A role must be specified when connecting to Snowflake. The ACCOUNTADMIN role is required to harvest the full range of metadata. Other roles provide access to basic metadata only, without extended metadata or lineage information. When using a role other than ACCOUNTADMIN, grant the role-specific permissions outlined in this task.

Some collector features require executing queries in Snowflake, which requires a warehouse. If the user credentials have a default warehouse configured, no additional warehouse configuration is needed. To use a different warehouse, or if no default warehouse is set, specify the warehouse using the Snowflake Warehouse configuration option.

## Procedure

1.  Create a role and grant warehouse permissions.

    ```
    CREATE OR REPLACE ROLE DDW_ACCOUNT_ROLE;
                            GRANT OPERATE, USAGE ON WAREHOUSE <warehouse_name> TO ROLE DDW_ACCOUNT_ROLE;
    ```

2.  Grant permissions to enable metadata harvesting for database, schema, tables, and views.

    ```
    GRANT USAGE ON DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                            GRANT USAGE ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                            GRANT SELECT ON ALL TABLES IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                            GRANT SELECT ON ALL EXTERNAL TABLES IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                            GRANT SELECT ON ALL VIEWS IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                            GRANT USAGE ON FUTURE SCHEMAS IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                            GRANT SELECT ON FUTURE TABLES IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
    ```

    **Note:** If you don't plan to use the Enable Sample String Values collection and Enable column statistics collection options, you can grant the REFERENCES permission instead of SELECT:

    ```
    GRANT USAGE ON DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                                GRANT USAGE ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                                GRANT REFERENCES ON ALL TABLES IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                                GRANT REFERENCES ON ALL EXTERNAL TABLES IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                                GRANT REFERENCES ON ALL VIEWS IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                                GRANT USAGE ON FUTURE SCHEMAS IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
                                GRANT REFERENCES ON FUTURE TABLES IN DATABASE <database_name> TO ROLE DDW_ACCOUNT_ROLE;
    ```

3.  Grant permissions to harvest the following: object dependency-based lineage, user-defined functions, data metric functions, stored procedures, tags and tag values, row access policies, masking policies, and table usage.

    **Important:** You need the ACCOUNTADMIN role to grant these permissions.

    There are two options for assigning these permissions:

    -   Option 1: Use the ACCOUNTADMIN role to grant broad imported privileges across databases:

        ```
        USE ROLE ACCOUNTADMIN;
                                    GRANT IMPORTED PRIVILEGES ON DATABASE SNOWFLAKE TO ROLE DDW_ACCOUNT_ROLE;
        ```

    -   Option 2: Assign specific database roles for targeted permission allocation:

        ```
        USE ROLE ACCOUNTADMIN;
                                    USE DATABASE SNOWFLAKE;
                                    GRANT DATABASE ROLE OBJECT_VIEWER TO ROLE DDW_ACCOUNT_ROLE;
                                    GRANT DATABASE ROLE GOVERNANCE_VIEWER TO ROLE DDW_ACCOUNT_ROLE;
        ```

        For more information about these database roles, see the [Snowflake documentation](https://docs.snowflake.com/en/sql-reference/snowflake-db.html).

4.  Grant permissions for Streamlit apps.

    These permissions are only required if you want to harvest metadata from Streamlit apps:

    ```
    GRANT USAGE ON STREAMLIT <streamlit_app_name> TO ROLE DDW_ACCOUNT_ROLE;
    ```

5.  Create a dedicated Snowflake user for the collector.

    To create key-pair authentication for this user, you need a minimum of SECURITYADMIN role to alter the user settings. See the [Snowflake documentation](https://docs.snowflake.com/en/user-guide/key-pair-auth.html).

    ```
    CREATE USER DDW_ACCOUNT
                            RSA_PUBLIC_KEY = '<rsa_public_key>'
                            TYPE = SERVICE
                            DEFAULT_ROLE = DDW_ACCOUNT_ROLE
                            DEFAULT_WAREHOUSE = '<warehouse_name>'
                            DISPLAY_NAME = 'data.world';
                            
                            GRANT ROLE DDW_ACCOUNT_ROLE TO USER DDW_ACCOUNT;
    ```

6.  Grant user access to the warehouse.

    ```
    GRANT USAGE ON WAREHOUSE <warehouse_name> TO ROLE DDW_ACCOUNT_ROLE;
    ```

7.  Verify that the appropriate permissions are granted.

    Run the following query:

    ```
    SHOW GRANTS TO ROLE DDW_ACCOUNT_ROLE;
    ```


**Parent Topic:**[Snowflake metadata collector](../concept/snowflake-metadata-collector.md)

