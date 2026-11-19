---
title: Configure the Cloud Asset Collection Configs table
description: Configure the Cloud Asset Collection Configs table to collect cloud assets or add comments to the CI entries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/cloud-account-management/configure-cloud-asset-collection-table.html
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-11-17"
reading_time_minutes: 2
keywords: [cloud asset collection, asset collection configuration]
breadcrumb: [Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Configure the Cloud Asset Collection Configs table

Configure the Cloud Asset Collection Configs table to collect cloud assets or add comments to the CI entries.

## Before you begin

-   The cloud CIs must be discovered and stored in the CMDB.
-   The Cloud Account management plugin `(sn_itom_cam)` must be installed and active on your instance.

Role required: sn\_itom\_cam.cw\_admin

## About this task

Cloud asset explorer builds one list of your cloud configuration items \(CIs\) and their key relationships. A scheduled job refreshes the list every 30 minutes. The list includes only the CI classes that are marked active in the Cloud Asset Collection Configs table, and the job skips any CI class that isn't active. For more information about how the list is kept up to date, see [Viewing cloud assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/viewing-cloud-assets.md).

The Cloud Asset Collection Configs table includes six CI class records. You can't add new records. For descriptions of the table fields, see [Cloud Asset Collection table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/cloud-account-management/cloud-asset-collection-table.md).

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace**.

2.  Remove the text in the URL after \*service-now.com/ and enter the table name `sn_itom_cam_asset_collection_config_list.do`.

    The table entries are as follows.

    \[Omitted image "cloud-asset-collection.png"\] Alt text: Cloud Asset Collection Configs

3.  Double-click an entry to update the Active or Comments column, then select the Save icon\[Omitted image "save-icon.png"\] Alt text: Save.

    **Note:** You can stop collecting cloud assets by setting the Active column as false.

4.  Set the batch size by updating the **sn\_itom\_cam.cmdb.query.batchsize** system property.

    The default is 10,000 records per batch. Reduce the batch size if records are missing after the first run because the batch size is too large for the available nodes.

5.  Open the **Populate Flat Table With CI Assets Job** scheduled job and confirm that it is active.

    The job runs every 30 minutes.

6.  Confirm that the **Populate Asset Summary Table** scheduled job is active.

    This job also runs every 30 minutes and populates the aggregation table that provides the asset counts by category and provider.

7.  Wait for the first run to finish.

    The first run is the initial load of all existing CIs. Large CMDB tables can take longer. Each run handles the CI classes in order, and a run is skipped if the previous run is still in progress.


## Result

After the first run finishes, verify the results in Cloud asset explorer:

-   The Cloud assets page lists assets for each CI class that you marked active.
-   Filtering by category and subcategory returns results quickly. Changing the provider filter also returns results quickly.
-   For virtual machine instances, the service account, logical data center, image, hardware, and server fields are filled.
-   The counts by category and provider match the assets in the list.

If an asset is missing from Cloud asset explorer, see .

