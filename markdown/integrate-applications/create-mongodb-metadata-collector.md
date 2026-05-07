---
title: Create a MongoDB metadata collector
description: Create a collector to import metadata from MongoDB.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MongoDB metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a MongoDB metadata collector

Create a collector to import metadata from MongoDB.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](../concept/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the MongoDB collector](prepare-to-run-mongodb-collector.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **MongoDB**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field cannot be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

6.  Enter the MongoDB connection details.

    |Field|Description|
    |-----|-----------|
    |Connection String|[Connection string](https://www.mongodb.com/docs/manual/reference/connection-string-options/) for your MongoDB cluster or instance. Make sure that any option parameters in the connection string are URL-encoded.|

7.  Enter the MongoDB configuration details.

<table id="table_nyc_qqp_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Included Databases

</td><td>

Databases to collect. Provide database names or regular expressions. List only one database per line. Databases matching any specified expression are collected.

</td></tr><tr><td>

Excluded Databases

</td><td>

Databases to exclude from collection. Provide database names or regular expressions. List only one database per line. Databases matching any specified expression are excluded. Included databases take precedence over excluded databases.

</td></tr><tr><td>

Analysis Samples Count

</td><td>

Number of documents sampled from each collection for [field type analysis](https://www.mongodb.com/docs/manual/reference/operator/aggregation/sample/). This field must be a non-negative integer.Default: 1000.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](../concept/manage-data-catalog.md).

**Parent Topic:**[MongoDB metadata collector](../concept/mongodb-metadata-collector.md)

