---
title: Create an Amazon S3 metadata collector
description: Use a metadata collector to import Amazon S3 bucket and object metadata into the data catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-amazon-s3-metadata-collector.html
release: australia
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 4
keywords: [Amazon S3 metadata collector]
breadcrumb: [Amazon S3 metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create an Amazon S3 metadata collector

Use a metadata collector to import Amazon S3 bucket and object metadata into the data catalog.

## Before you begin

-   A MID Server must be set up for the collectors. For more information, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mid-server-for-metadata-collectors-dc.md).
-   All prerequisite tasks must be complete. For more information, see [Prepare to run the Amazon S3 collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prepare-to-run-amazon-s3-collector.md).

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

    |Field|Description|
    |-----|-----------|
    |AWS Region|The AWS region used to start the S3 client.|

8.  Configure the authentication options.

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

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-data-catalog.md).

**Parent Topic:**[Amazon S3 metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/amazon-s3-metadata-collector.md)

