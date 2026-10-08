---
title: Create a MongoDB metadata collector
description: Create a collector to import metadata from MongoDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/create-mongodb-metadata-collector.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [MongoDB metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a MongoDB metadata collector

Create a collector to import metadata from MongoDB.

## Before you begin

Before you begin, verify the following:

-   All per-requisite tasks are completed. For more information, see [Prepare to run the MongoDB collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/prepare-to-run-mongodb-collector.md).
-   If you plan to run the collector on-premise, a MID Server is setup for the collector. For more information, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/mid-server-for-metadata-collectors-dc.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub \[Omitted image "wdf-connect-hub-icon.png"\] Alt text: Connect Hub icon icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **MongoDB**.

5.  From the Connection type list, select one of the following:

    1.  Select **New connection** to configure a new connection.

    2.  Select **Existing connection** to reuse an existing connection and select an existing connection from the **Connections** list.

        The configuration form is filled with details from the existing connection. The name is appended with the word Copy and sensitive details like password aren't copied.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field can't be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

7.  Configure the connection options.

<table id="table_s3_collector_props"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use MID server

</td><td>

Option to connect to the source system through a MID Server. When selected, the **MID selection** options appear.

</td></tr><tr><td>

MID selection

</td><td>

MID Server routing option for the collector job. This field appears only when **Use MID server** is selected.

 -   **Auto-Select MID Server** — The system selects an available MID Server at job execution time. Default selection.
-   **Specific MID Server** — The collector job runs on the selected MID Server. If the MID Server is offline at job execution time, the job fails with an error identifying the MID Server by name.
-   **Specific MID Cluster** — The collector job runs on any available MID Server within the selected cluster.


</td></tr><tr><td>

MID Server

</td><td>

MID Server to use for the collector job. This field appears only when **Specific MID Server** is selected. The selected MID Server is saved on the collector record and used for all subsequent collection runs until changed.

</td></tr><tr><td>

MID Cluster

</td><td>

MID cluster to use for the collector job. This field appears only when **Specific MID Cluster** is selected. The selected cluster is saved on the collector record; any available MID Server within the cluster may serve the job.

</td></tr><tr><td>

Capabilities

</td><td>

One or more capability labels that restrict auto-selection to MID Servers advertising those capabilities. This field appears only when **Auto-Select MID Server** is selected.

</td></tr><tr><td>

MID application

</td><td>

MID Server application to use for the collector job. This field appears only when **Auto-Select MID Server** is selected.

</td></tr></tbody>
</table>8.  Enter the MongoDB connection details.

    |Field|Description|
    |-----|-----------|
    |Connection String|[Connection string](https://www.mongodb.com/docs/manual/reference/connection-string-options/) for your MongoDB cluster or instance. Make sure that any option parameters in the connection string are URL-encoded.|

9.  Enter the MongoDB configuration details.

    |Field|Description|
    |-----|-----------|
    |Included Databases|Databases to collect. Provide database names or regular expressions. List only one database per line. Databases matching any specified expression are collected.|
    |Excluded Databases|Databases to exclude from collection. Provide database names or regular expressions. List only one database per line. Databases matching any specified expression are excluded. Included databases take precedence over excluded databases.|

10. Configure the advanced options.

<table id="table_oxn_jh5_rjc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Analysis samples count

</td><td>

Number of documents sampled from each collection for [field type analysis](https://www.mongodb.com/docs/manual/reference/operator/aggregation/sample/). This field must be a non-negative integer.Default: 1000.

</td></tr></tbody>
</table>11. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/manage-data-catalog.md).

**Parent Topic:**[MongoDB metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/mongodb-metadata-collector.md)

