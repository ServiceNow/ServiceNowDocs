---
title: Create a BigQuery metadata collector
description: Create a collector to import metadata from BigQuery.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [BigQuery metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a BigQuery metadata collector

Create a collector to import metadata from BigQuery.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](../concept/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the BigQuery collector](prepare-to-run-bigquery-collector.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **BigQuery**.

5.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field cannot be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

6.  Enter the BigQuery authentication details.

    |Field|Description|
    |-----|-----------|
    |BigQuery Credential File Path|Upload the credentials file [you generated](create-bigquery-metadata-collector.md) for authentication.|

7.  Enter the BigQuery configuration details.

    |Field|Description|
    |-----|-----------|
    |BigQuery Project|BigQuery project that contains the datasets to catalog.|
    |BigQuery Datasets to Catalog|BigQuery datasets to catalog in the project. By default, all datasets in a project are cataloged. When multiple projects are specified, the dataset filter applies to all projects.|

8.  Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](../concept/manage-data-catalog.md).

**Parent Topic:**[BigQuery metadata collector](../concept/bigquery-metadata-collector.md)

