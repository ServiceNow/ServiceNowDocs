---
title: Prepare to run the MySQL collector
description: Create a MySQL user and grant permissions before running the collector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prepare-to-run-mysql-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MySQL metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the MySQL collector

Create a MySQL user and grant permissions before running the collector.

## Before you begin

Role required: admin

## About this task

Configure a MySQL user with the minimum required permissions for metadata harvesting.

## Procedure

1.  Create a user.

    ```
    CREATE USER 'catalog_user'@'%' IDENTIFIED BY '<password>';
    ```

    Replace `<password>` with a secure password.

2.  Grant permissions to the user.

    ```
    GRANT SELECT, SHOW VIEW, EXECUTE ON *.* TO 'catalog_user'@'%';
    ```

    This grants the following permissions:

    -   SELECT: Read access to tables and views
    -   SHOW VIEW: View definition access
    -   EXECUTE: Stored procedure and function access

**Parent Topic:**[MySQL metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/mysql-metadata-collector.md)

