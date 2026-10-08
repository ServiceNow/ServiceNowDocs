---
title: Create an Amazon S3 metadata collector
description: Use a metadata collector to import Amazon S3 bucket and object metadata into the data catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/create-amazon-s3-metadata-collector.html
release: australia
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 5
keywords: [Amazon S3 metadata collector]
breadcrumb: [Amazon S3 metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create an Amazon S3 metadata collector

Use a metadata collector to import Amazon S3 bucket and object metadata into the data catalog.

## Before you begin

-   All prerequisite tasks must be complete. For more information, see [Prepare to run the Amazon S3 collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/prepare-to-run-amazon-s3-collector.md).
-   If you plan to run the collector on-premise, a MID Server is setup for the collector. For more information, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/mid-server-for-metadata-collectors-dc.md).

Role required: connection-admin.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub \[Omitted image "wdf-connect-hub-icon.png"\] Alt text: Connect Hub icon icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **Amazon S3**.

5.  From the Connection type list, select one of the following:

    1.  Select **New connection** to configure a new connection.

    2.  Select **Existing connection** to reuse an existing connection and select an existing connection from the **Connections** list.

        The configuration form is filled with details from the existing connection. The name is appended with the word Copy and sensitive details like password aren't copied.

6.  Complete the form.

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

</td></tr><tr><td>

AWS Region

</td><td>

The AWS region used to start the S3 client.

</td></tr></tbody>
</table>8.  Configure the authentication options.

    |Field|Description|
    |-----|-----------|
    |Authenticate using AWS Key/Secret|Specify the **AWS Access Key ID** and **AWS Secret Access Key**.|
    |Authenticate using IAM role|Specify the **AWS IAM role ARN** and **AWS Role External ID**.|

9.  Configure the bucket and objects options.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Excluded bucket

</td><td>

Specify the buckets to exclude. You can provide the bucket name or a regular expression to match. Use the parameter multiple times for multiple specific buckets. If multiple regular expressions are specified, the collector excludes buckets that match any of them. If both **Include bucket** and **Excluded bucket** are specified, **Include bucket** takes precedence.

 **Note:** If the bucket name includes special characters \[. , + , \* , ? , ^ , $ , \( , \) , \[ , \] , \{ , \} , \| , \\\], use a backslash \(\\\) before the special character to escape it. For example, \\\[

</td></tr><tr><td>

Included bucket

</td><td>

Specify the buckets to collect. You can provide the bucket name or a regular expression to match. Use the parameter multiple times for multiple specific buckets. If multiple regular expressions are specified, the collector harvests buckets that match any of them.

 **Note:** If the bucket name includes special characters \[. , + , \* , ? , ^ , $ , \( , \) , \[ , \] , \{ , \} , \| , \\\], use a backslash \(\\\) before the special character to escape it. For example, \\\[

</td></tr><tr><td>

Include object prefix

</td><td>

Specify the object prefix to harvest objects that begin with the specified prefix.

</td></tr><tr><td>

Included object

</td><td>

Specify the objects to collect, using either an object name or a regular expression to match. Use the parameter multiple times for multiple specific objects. If multiple regular expressions are specified, the collector harvests objects that match any of them. If both **Included object** and **Excluded object** are specified, **Included object** takes precedence.

 **Note:** If the object name includes special characters \[. , + , \* , ? , ^ , $ , \( , \) , \[ , \] , \{ , \} , \| , \\\], use a backslash \(\\\) before the special character to escape it. For example, \\\[

</td></tr><tr><td>

Excluded object

</td><td>

Specify the objects not to collect, using either an object name or a regular expression to match. Use the parameter multiple times for multiple specific objects. If multiple regular expressions are specified, the collector excludes objects that match any of them. If both **Included object** and **Excluded object** are specified, **Included object** takes precedence.

 **Note:** If the object name includes special characters \[. , + , \* , ? , ^ , $ , \( , \) , \[ , \] , \{ , \} , \| , \\\], use a backslash \(\\\) before the special character to escape it. For example, \\\[

</td></tr></tbody>
</table>10. Configure the advanced options.

    |Field|Description|
    |-----|-----------|
    |Max objects per run|Maximum resources the collector will harvest, up to 10 million. If not specified, by default the collector will harvest a maximum of 10,000 resource.|

11. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/manage-data-catalog.md).

**Parent Topic:**[Amazon S3 metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/amazon-s3-metadata-collector.md)

