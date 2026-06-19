---
title: Create an Azure Data Factory metadata collector
description: Create a collector to import metadata from Azure Data Factory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/create-azure-data-factory-metadata-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Azure Data Factory metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create an Azure Data Factory metadata collector

Create a collector to import metadata from Azure Data Factory.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the Azure Data Factory collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-azure-data-factory-collector.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub \[Omitted image "wdf-connect-hub-icon.png"\] Alt text: Connect Hub icon icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **Azure Data Factory**.

5.  From the Connection type list, select one of the following:

    1.  Select **New connection** to configure a new connection.

    2.  Select **Existing connection** to reuse an existing connection and select an existing connection from the **Connections** list.

        The configuration form is filled with details from the existing connection. The name is appended with the word Copy and sensitive details like password aren't copied.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field can't be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

7.  Enter the Azure Data Factory authentication details.

    |Field|Description|
    |-----|-----------|
    |Microsoft Entra client ID|Azure Active Directory application client ID for the Azure Data Factory app.|
    |Microsoft Entra client secret|Azure Active Directory application client secret for the Azure Data Factory app.|
    |Azure subscription ID|The subscription ID in which the data factories are available.|
    |Microsoft Entra Tenant ID|Azure Active Directory application tenant ID for the Azure Data Factory app.|

8.  Enter the Azure Data Factory configuration details.

    |Field|Description|
    |-----|-----------|
    |Include Data Factory name\(s\)|Names of data factories to catalog. Enter either the exact name or a regular expression to match. List one data factory name per line.|
    |Exclude Data Factory name\(s\)|Names of data factories to exclude from cataloging. Enter either the exact name or a regular expression to match. List one data factory name per line.|

9.  Configure the advanced options.

<table id="table_ocr_gc4_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max retries

</td><td>

The number of times the system retries a failed API call.Default: 5

</td></tr><tr><td>

Retry delay

</td><td>

The number of seconds to wait between retry attempts for a failed API call.Default: 2 seconds

</td></tr></tbody>
</table>10. Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/manage-data-catalog.md).

**Parent Topic:**[Azure Data Factory metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/azure-data-factory-metadata-collector.md)

