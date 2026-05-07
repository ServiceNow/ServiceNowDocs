---
title: Prepare to run the PostgreSQL collector
description: Create a PostgreSQL user and configure permissions before running the collector.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PostgreSQL metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the PostgreSQL collector

Create a PostgreSQL user and configure permissions before running the collector.

## Before you begin

Role required: admin

## Procedure

1.  Create a new role.

    ```
    CREATE ROLE ddw_role;
    ```

2.  Grant metadata harvesting permissions to the role.

    ```
    GRANT SELECT ON ALL TABLES IN SCHEMA information_schema TO ddw_role;
    GRANT SELECT ON ALL TABLES IN SCHEMA "<schemaName>" TO ddw_role;
    GRANT SELECT ON TABLE pg_namespace TO ddw_role;
    GRANT SELECT ON TABLE pg_class TO ddw_role;
    GRANT SELECT ON TABLE pg_description TO ddw_role;
    GRANT SELECT ON TABLE pg_attribute TO ddw_role;
    GRANT SELECT ON TABLE pg_type TO ddw_role;
    GRANT SELECT ON TABLE pg_attrdef TO ddw_role;
    GRANT SELECT ON TABLE pg_index TO ddw_role;
    GRANT SELECT ON TABLE pg_proc TO ddw_role;
    GRANT SELECT ON TABLE pg_database TO ddw_role;
    GRANT SELECT ON TABLE pg_matviews TO ddw_role;
    ```

    Replace `<schemaName>` with your schema name.

3.  Grant permissions for column statistics harvesting.

    Run these commands for each database and schema you want to collect statistics from:

    ```
    GRANT USAGE ON SCHEMA "<schemaName>" TO ddw_role;
     GRANT SELECT ON ALL TABLES IN SCHEMA "<schemaName>" TO ddw_role;
    ```

    Replace `<schemaName>` with your schema name.

4.  Create a user and assign the role.

    ```
    CREATE USER ddw_user PASSWORD '<password>';
    GRANT ddw_role TO ddw_user;
    ```

    Replace `<password>` with a secure password.

5.  Configure IAM authentication.

    See the [AWS IAM authentication documentation](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.IAMDBAuth.html) for setup instructions.


**Parent Topic:**[PostgreSQL metadata collector](../concept/postgresql-metadata-collector.md)

