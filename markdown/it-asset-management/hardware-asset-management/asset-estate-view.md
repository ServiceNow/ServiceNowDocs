---
title: Asset estate view
description: Use the Asset estate view in the Hardware Asset Workspace to view the asset functions and notifications such as expiring assets, expiring lease contracts, and take appropriate actions.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Asset estate view

Use the Asset estate view in the Hardware Asset Workspace to view the asset functions and notifications such as expiring assets, expiring lease contracts, and take appropriate actions.

![Asset estate view in Hardware asset workspace](../image/asset-estate.png "Asset estate view")

**Note:** The Software license tab is hidden when Software Asset Management \(com.snc.software\_asset\_management\) or Software Asset Management Professional \(com.snc.pa.samp\) is active. You can view this Software license tab in Software Asset Workspace.

|Widget or chart|Description|
|---------------|-----------|
|Hardware warranty expiration this year|Count of hardware and consumable assets that are expiring this current year.|
|Lease contract expiration this year|Count of lease contract models expiring this current year.|
|Asset requests|Count of hardware, consumable, and bundle requests in the catalog.|
|Refresh requests|Count of assets that are pending refresh.|
|Asset lifecycle by state|Number of assets grouped by the life cycle state such as Retired, In use, In stock.|
|Assets eligible for refresh|Assets nearing the end of life and which are eligible for refresh.|
|Assets by model category|Number of assets grouped by the model category such as Software License, Consumable, Server.|
|End of life method \(YTD\)|Assets retired until date in this current year.|
|Incomplete assets by model category|Asset models without purchase order number, purchase order line, or receiving line.|
|Spend by model category|Cost of assets grouped by their model category.|
|Asset incident frequency|Assets that have been reported with frequent incidents.|
|Hardware assets disposed \(YTD\) by model category|Assets disposed until the current date in this year and grouped by their model category.|

To create hardware, software, consumable, bundle, pallet, mobile, and facility assets, select **New asset**. For more details, see [Create assets](../../asset-management/task/t_CreatingAssets.md).

## Load reports on Asset estate view

You can load charts or widgets that fetch a huge set of asset records on demand instead of loading them along with the page. This approach enables you to reduce the loading time for the Asset estate view.

The system property **sn\_itam\_workspace.asset\_estate\_enable\_lazy\_loading** provides you with an option to either selectively load reports you want to view or load reports concurrently with the page. By default, this system property is set to **False**. When this system property is enabled on your ServiceNow instance, you can view charts or widgets by using the **Load report** option.

![Load reports on Asset estate view](../image/ham-asset-estate-load.png "Load reports on Asset estate view")

