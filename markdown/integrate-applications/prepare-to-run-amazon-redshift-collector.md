---
title: Prepare to run the Amazon Redshift collector
description: Create a Redshift user and configure permissions before running the collector.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Amazon Redshift metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Amazon Redshift collector

Create a Redshift user and configure permissions before running the collector.

## Before you begin

Role required: admin

## About this task

Run the following SQL statements to set up a new user with appropriate permissions to harvest from Redshift. For information about Redshift permissions, see the [Redshift GRANT documentation](https://docs.aws.amazon.com/redshift/latest/dg/r_GRANT.html).

## Procedure

1.  Create a user.

    ```
    CREATE USER ddw_user PASSWORD '<password>';
    ```

    Replace `<password>` with a secure password.

2.  Grant permissions to the user.

    Run these commands for each schema you want to collect. Replace `<schemaName>` with your schema name.

    ```
    -- Grant USAGE access to the target schema
                  GRANT USAGE ON SCHEMA <schemaName> TO ddw_user;
              -- Grant USAGE access to pg_catalog schema for stored procedures and extended metadata
                  GRANT USAGE ON SCHEMA pg_catalog TO ddw_user;
              -- Grant SELECT access on all tables in the target schema
                  GRANT SELECT ON ALL TABLES IN SCHEMA <schemaName> TO ddw_user;
              -- Grant SELECT access on all tables in pg_catalog schema for stored procedures and extended metadata
                  GRANT SELECT ON ALL TABLES IN SCHEMA pg_catalog TO ddw_user;
    ```


**Parent Topic:**[Amazon Redshift metadata collector](../concept/amazon-redshift-metadata-collector.md)

