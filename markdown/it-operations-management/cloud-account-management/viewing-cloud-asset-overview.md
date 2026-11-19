---
title: Viewing the cloud asset overview
description: The Cloud asset overview page summarizes your discovered cloud assets by provider and category, so you can see how many assets you have across AWS, Azure, GCP, and OCI at a glance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/viewing-cloud-asset-overview.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-11-11"
reading_time_minutes: 1
keywords: [cloud asset overview, cloud assets]
breadcrumb: [Viewing the Cloud asset explorer, Viewing Cloud Account Management dashboards, Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Viewing the cloud asset overview

The Cloud asset overview page summarizes your discovered cloud assets by provider and category, so you can see how many assets you have across AWS, Azure, GCP, and OCI at a glance.

To open the page, navigate to **All** &gt; **Cloud Workspace** &gt; **Monitor and track** &gt; **Cloud asset explorer** &gt; **Overview**.

The page shows one tile for each cloud provider. Each tile shows the number of AWS accounts, Azure subscriptions, GCP projects, or OCI accounts, and the number of assets in each of these categories:

-   Compute
-   Databases
-   Load balancers and network
-   Storage

\[Omitted image "cam-cloud-asset-overview.png"\] Alt text: Cloud asset overview page with a tile for each cloud provider

Select a number to view the matching assets.

The counts reflect the most recent refresh of your asset data. For more information about how the data is collected and refreshed, see [Viewing cloud assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/viewing-cloud-assets.md).

The counts include only the CI classes that are marked active in the Cloud Asset Collection Configs table. To choose which CI classes are collected, see [Configure the Cloud Asset Collection Configs table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configure-cloud-asset-collection-table.md).

**Parent Topic:**[Viewing the Cloud asset explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/viewing-cloud-asset-explorer.md)

