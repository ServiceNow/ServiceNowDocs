---
title: Create a SQL Server Reporting Services metadata collector
description: Create a collector to import metadata from SQL Server Reporting Services \(SSRS\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-sql-server-reporting-services-metadata-collector.html
release: brazil
topic_type: task
last_updated: "2026-09-16"
reading_time_minutes: 5
breadcrumb: [SQL Server Reporting Services \(SSRS\) metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a SQL Server Reporting Services metadata collector

Create a collector to import metadata from SQL Server Reporting Services \(SSRS\).

## Before you begin

Before you begin, verify the following:

-   All per-requisite tasks are completed. For more information, see [Prepare SSRS for metadata collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/preparing-to-run-sql-server-reporting-services-collector.md).
-   If you plan to run the collector on-premise, a MID Server is setup for the collector. For more information, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/mid-server-for-metadata-collectors-dc.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub \[Omitted image "wdf-connect-hub-icon.png"\] Alt text: Connect Hub icon icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **SSRS**.

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

Report server web service URL

</td><td>

The Base URL of the SSRS API. For example, https://ssrs-server.mycompany.com/reports/api/v2.0

</td></tr><tr><td>

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
</table>8.  Configure the authentication options.

    |Field|Description|
    |-----|-----------|
    |Domain username|SSRS username for authentication.|
    |Domain user password|Password of the user.|
    |Authentication type|Select from **Basic** or **NTLM**.|
    |NTLM domain|Provide the NTLM domain to authenticate with. Applicable only when the authentication type is NTML.|
    |SSL certificate|Upload a certificate for a self-signed or custom SSRS server. Leave empty to trust all certificates.|

9.  Set the Configuration options.

    |Field|Description|
    |-----|-----------|
    |Include folder paths|Specify the folders to be collected. You can either provide the folder paths or a regular expression to match. Use the parameter multiple times for multiple specific folders. If multiple regular expressions are specified, the collector will harvest folders that match any of them. If empty, all folders are included.|
    |Exclude folder paths|Specify the folders to be excluded by the collector. You can either provide the folder paths or a regular expression to match. Use the parameter multiple times for multiple specific tables. If multiple regular expressions are specified, the collector will exclude folders that match any of them. If both Include folder and Exclude folder paths are specified, Include table takes precedence.|

10. Configure the advanced options.

<table id="table_ocr_gc4_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable lineage collection

</td><td>

Disable collection of lineage relationships between reports and their data sources and datasets.

</td></tr><tr><td>

Disable extended metadata collection

</td><td>

Skips collection of Data Sources and Policies, which require an elevated SSRS role beyond Browser.

</td></tr><tr><td>

Pagination size

</td><td>

The number of records per SSRS API page request. Default limit of per page is 200 records and max limit of per page is 2000 records.

</td></tr><tr><td>

Max retries

</td><td>

Number of times the system retries a failed API call. Default: 5

</td></tr><tr><td>

Retry delay

</td><td>

Number of seconds to wait between retry attempts for a failed API call. Default: 2 seconds

</td></tr></tbody>
</table>11. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/manage-data-catalog.md).

**Parent Topic:**[SQL Server Reporting Services \(SSRS\) metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/sql-server-reporting-services-collector.md)

