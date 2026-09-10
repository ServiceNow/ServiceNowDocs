---
title: Create a Salesforce metadata collector
description: Create a collector to import metadata from Salesforce.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-salesforce-metadata-collector.html
release: australia
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 3
breadcrumb: [Salesforce metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a Salesforce metadata collector

Create a collector to import metadata from Salesforce.

## Before you begin

Before you begin, verify the following:

-   All per-requisite tasks are completed. For more information, see [Prepare to run the Salesforce collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prepare-to-run-the-salesforce-collector.md).
-   If you plan to run the collector on-premise, a MID Server is setup for the collector. For more information, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mid-server-for-metadata-collectors-dc.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub \[Omitted image "wdf-connect-hub-icon.png"\] Alt text: Connect Hub icon icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **Salesforce**.

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

Enable the **Use MID server** toggle to connect to the source system through a MID Server. The system automatically selects an available MID Server.

</td></tr><tr><td>

Salesforce Hostname

</td><td>

The host name of the Salesforce instance using the following format: &lt;organization\_domain&gt;&lt;--optional-sandbox\_name.sandbox&gt;.my.salesforce.com. Do not include the protocol https.

 For example, for a production environment, it might look like acme.my.salesforce.com, and for a sandbox environment, it could be acme--dev.sandbox.my.salesforce.com

</td></tr></tbody>
</table>8.  Configure the authentication options.

    |Field|Description|
    |-----|-----------|
    |Connected app client ID|OAuth client ID for the Salesforce connected app on the instance.|
    |Connected app client secret|OAuth client secret for the Salesforce connected app on the instance.|
    |Username|The username to use to make the JDBC connection.|
    |Password|The password of the user.|
    |Security Token|Personal security token for the provided [Salesforce credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prepare-to-run-the-salesforce-collector.md).|

9.  Configure the connection and reliability options.

<table id="table_njt_klb_gkc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Query batch size

</td><td>

Number of Salesforce objects to query as a batch.Default: 20

</td></tr><tr><td>

Related object depth

</td><td>

Number of related \(parent-child\) object relationships to navigate. Default is to navigate all relationships.

</td></tr><tr><td>

Include objects

</td><td>

Specify one or more regular expressions to match Salesforce objects that should be included. Default is to include all objects.

</td></tr><tr><td>

Max retries

</td><td>

Number of times the system retries a failed API call. Default: 5

</td></tr><tr><td>

Retry delay

</td><td>

Number of seconds to wait between retry attempts for a failed API call. Default: 2 seconds

</td></tr></tbody>
</table>10. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-data-catalog.md).

**Parent Topic:**[Salesforce metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/salesforce-metadata-collector.md)

