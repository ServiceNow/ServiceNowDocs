---
title: Hardware asset overview
description: Enhance your Asset Management experience by using the modernized and user-friendly Hardware asset overview view. The Hardware asset overview is a simplified and intuitive environment that helps you use the application more effectively by reducing complexity.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Asset Management, IT Asset Management]
---

# Hardware asset overview

Enhance your Asset Management experience by using the modernized and user-friendly Hardware asset overview view. The Hardware asset overview is a simplified and intuitive environment that helps you use the application more effectively by reducing complexity.

Use the Hardware asset overview view to:

-   Act on discrepancies such as when an asset is missing PO number, model number, asset function, or manufacturer.
-   Navigate to specific dashboards on asset functions such as Asset requests, Transfer orders, and Stock orders.
-   View the 360 asset view section displaying asset counts by model category and asset value by model category.
-   View the overall performance section displaying the Discovered and undiscovered asset count and Assets eligible for refresh by model category.

Select any widget or chart to view detailed information and take appropriate actions. You can also use **Location**, **Stockroom**, and **Model category** lists to filter your results.

![Hardware asset overview in Asset Workspace](../../hardware-asset-management/image/asset-wrkspc-assetoverview.png "Hardware asset overview")

|Widget or chart|Description|
|---------------|-----------|
|Asset requests|Number of requested items where the item’s model is hardware, consumable, or bundle.|
|Transfer orders|Number of active transfer orders.|
|Stock orders|Number of requested hardware inventory stock order items.|

|Widget or chart|Description|
|---------------|-----------|
|Asset count by model category|Number of assets grouped by the model category such as Consumable, Computer, and Mobile Device.|
|Asset value by model category|Cost of assets grouped by the model category such as Software License, Consumable, and Server.|

|Widget or chart|Description|
|---------------|-----------|
|Discovered and undiscovered asset count|Comparison of the number of discovered and undiscovered assets grouped by model category. Undiscovered assets are the assets that aren’t discovered at all or not discovered within one month.|
|Assets eligible for refresh by model category|Number of assets that have already expired or the current day is the expiry date, and are eligible for a refresh.|

## Load reports on Hardware asset overview

You can load charts or widgets that fetch a huge set of asset records on demand instead of loading them along with the page. This approach enables you to reduce the loading time for the Hardware asset overview page.

The system property **sn\_itam\_workspace.asset\_overview\_enable\_lazy\_loading** provides you with an option to either selectively load reports you want to view or load reports concurrently with the page. By default, this system property is set to **False**. When this system property is enabled on your ServiceNow instance, you can view reports by using the **Load report** option.

![Load report option on Hardware asset overview page](../../hardware-asset-management/image/asset-workspace-overview-load.png "Load reports on Hardware Asset overview")

