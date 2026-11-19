---
title: Viewing cloud assets
description: This page displays the Cloud assets view. It lists all compute assets across connected cloud providers such as AWS, Azure, GCP, and OCI. Details include location, cloud account, installation status, owner, discovered dates, ownership attestation, and cost center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/viewing-cloud-assets.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-11-19"
reading_time_minutes: 3
breadcrumb: [Viewing the Cloud asset explorer, Viewing Cloud Account Management dashboards, Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Viewing cloud assets

This page displays the Cloud assets view. It lists all compute assets across connected cloud providers such as AWS, Azure, GCP, and OCI. Details include location, cloud account, installation status, owner, discovered dates, ownership attestation, and cost center.

As an admin, you can access the dashboard by navigating to **All** &gt; **Cloud Workspace** &gt; **Monitor and track** &gt; **Cloud asset explorer** &gt; **Cloud assets**

The Cloud assets page lists the assets across all cloud providers. Select a category, such as All compute assets, and then use the Provider, Region, Owner, Cost center, and Cloud account filters to narrow the list. You can also refine the list with conditions, sorting, and grouping.

\[Omitted image "cloud-assets.png"\] Alt text: Cloud assets

Click the respective name to view the details.

**Note:** Duplicate LDC entries no longer appear in the Region filter in Cloud Asset Explorer. After upgrading your instance to the latest version, the Region filter may be empty until the background job completes its initial run. Depending on data volume, this can take several hours. The job runs approximately every 30 minutes automatically.

\[Omitted image "cloud-asset-details.png"\] Alt text: cloud asset details

In Asset Explorer, retired configuration items \(CIs\) remain in the asset table as long as they exist in the CMDB, even after retirement. To manage this, users can configure a custom retention period \(in seconds\) that automatically removes retired CIs from the asset table after the defined duration. For example, setting the property to 86,400 seconds \(1 day\) ensures that a retired CI is removed from the asset table one day after retirement. The CI may continue to exist in the CMDB. This helps improve performance for high-volume environments by ensuring that only active CIs remain in the asset table.

For more information about the various sections, see [Managing the Cloud Account Management cloud asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/manage-cam-ci-details.md).

## How asset data is kept up to date

Cloud asset explorer reads from a single list of cloud configuration items \(CIs\) and their key relationships. A scheduled job refreshes this list every 30 minutes.

-   The list includes only the CI classes that are marked active in the Cloud Asset Collection Configs table. To turn collection on or off for a CI class, see [Configure the Cloud Asset Collection Configs table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configure-cloud-asset-collection-table.md). For descriptions of the configuration fields, see [Cloud Asset Collection Configs table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/cloud-asset-collection-table.md).
-   The first run loads all existing CIs. Large CMDB tables can take longer.
-   Later runs add new CIs, update changed CIs and their relationships, and remove CIs that were deleted from the CMDB.
-   A run is skipped while the previous run is still in progress.
-   An asset appears in the list only if it has a relationship to a logical data center and a cloud service account in the CMDB.

## Security findings from SecOps

The integration requires the two SecOps applications that connect SecOps to Cloud Workspace \(scope: `sn_sec_icw`\). Install Cloud Workspace and SecOps applications.

When the SecOps integration with Cloud Workspace is set up, Cloud asset explorer shows the security findings for each cloud asset. You can see which assets have findings without leaving Cloud Workspace.

-   The Cloud assets list shows the total number of security findings for each asset in the **Total Security Findings** column.
-   The total adds the findings for each severity rating that is active in the SecOps configuration. By default, the active ratings are critical, high, and medium.
-   When you open an asset, its security findings appear on the **Security findings** tab.
-   The **Populate Security Findings Data in Assets Table** scheduled job copies the findings counts from SecOps onto the assets.

-   **[Managing the Cloud Account Management cloud asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/manage-cam-ci-details.md)**  
Use the cloud asset form in the Cloud Account Management to view, edit, and manage cloud asset details such as attributes, health, and records.

**Parent Topic:**[Viewing the Cloud asset explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/viewing-cloud-asset-explorer.md)

