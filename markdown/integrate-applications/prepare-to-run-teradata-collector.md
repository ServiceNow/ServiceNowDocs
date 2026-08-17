---
title: Prepare to run the Teradata Collector
description: Create a dedicated Teradata user with the permissions required for the metadata collector to harvest metadata from a target database.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/prepare-to-run-teradata-collector.html
release: australia
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 1
keywords: [Teradata, metadata collector, database user, permissions]
breadcrumb: [Teradata metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Teradata Collector

Create a dedicated Teradata user with the permissions required for the metadata collector to harvest metadata from a target database.

## Before you begin

Role required: admin

## About this task

The collector authenticates to Teradata using username and password. For more information, see the Teradata documentation on [Authentication Mechanisms](https://docs.teradata.com/r/ODBC-Driver-for-Teradata-User-Guide/June-2022/Network-Security/Authentication-Mechanisms).

## Procedure

1.  Create a Teradata user.

    ```
    CREATE USER <user> AS PERM=60000000 BYTES, PASSWORD=<password>
    ```

2.  Grant `SELECT` privileges on the target database and on DBC to the user.

    These grants allow the collector to harvest extended metadata for databases, tables, views, user defined functions, stored procedures, triggers, and user defined types.

    ```
    GRANT SELECT ON <database> TO <user>
    GRANT SELECT ON DBC TO <user>
    ```


## Result

The user has the permissions required to run the Teradata metadata collector.

## What to do next

Use these credentials when configuring the collector parameters. See [Create a Teradata metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-teradata-metadata-collector.md).

**Parent Topic:**[Teradata metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/teradata-metadata-collector.md)

