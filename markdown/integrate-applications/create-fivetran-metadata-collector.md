---
title: Create a Fivetran metadata collector
description: Create a collector to import metadata from Fivetran.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Fivetran metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Create a Fivetran metadata collector

Create a collector to import metadata from Fivetran.

## Before you begin

Before you begin, verify the following:

-   A MID Server is setup for the collectors. For more information, see [MID Server for metadata collectors](../concept/mid-server-for-metadata-collectors-dc.md).
-   All per-requisite tasks are completed. For more information, see [Prepare to run the Fivetran collector](prepare-to-run-fivetran-collector.md).
-   Role required: connection-admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Connect Hub ![Connect Hub icon](../../../build/workflow-data-fabric/image/wdf-connect-hub-icon.png) icon in the left sidebar.

3.  Select **Create** &gt; **Metadata collector**.

4.  From the System list, select **Fivetran**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection name|Unique identifier for the connection. This field cannot be modified once the connection is established.|
    |Short description|Purpose and details of the connection.|

6.  Enter the Fivetran authentication details.

    |Field|Description|
    |-----|-----------|
    |Fivetran API key|The Fivetran API key used to authenticate to the REST API.|
    |Fivetran API secret|The Fivetran secret used to authenticate to the REST API.|

7.  Enter the Fivetran configuration details.

    |Field|Description|
    |-----|-----------|
    |Exclude groups|Exclude the specified Fivetran group's contents from the catalog.|
    |Include only groups|Include only the specified Fivetran group's contents in the catalog.|

8.  Configure the advanced options.

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
</table>9.  Select **Save**.


## Result

The metadata collector is created and appears on the Connectors page with a Configured status. It is now ready to connect to the source system and harvest metadata.

## What to do next

After creating the collector, you can perform any of the following tasks:

-   Run the collector manually to harvest metadata immediately. See [Run metadata collectors manually](run_metadata-collectors-manually.md).
-   Automate metadata collection by scheduling regular collector runs. See [Schedule metadata collector runs](schedule-metadata-collector-runs.md).
-   Monitor execution status and troubleshoot issues by viewing the runtime logs. See [View runtime logs for collector runs](view-runtime-logs-for-collector-runs.md).
-   Discover and evaluate the harvested data assets in the Data Catalog. See [Governing the Data Catalog](../concept/manage-data-catalog.md).

**Parent Topic:**[Fivetran metadata collector](../concept/fivetran-metadata-collector.md)

