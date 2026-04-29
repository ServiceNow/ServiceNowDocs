---
title: Asset estate view
description: Use the Asset estate view in the Asset Workspace to create, view, and modify the assets and also manage asset functions and notifications.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Asset Management Workspace, Asset Management, IT Asset Management]
---

# Asset estate view

Use the Asset estate view in the Asset Workspace to create, view, and modify the assets and also manage asset functions and notifications.

**Note:** Software license tab is hidden when Software Asset Management \(com.snc.software\_asset\_management\) or Software Asset Management Professional \(com.snc.pa.samp\) is active. You can view this Software license tab in Software Asset Workspace.

![Asset estate view in Asset Workspace](../../hardware-asset-management/image/asset-wrkspc-assetestate.png "Asset estate view")

|Chart or widget|Description|
|---------------|-----------|
|Hardware warranty expiration this year|Count of hardware and consumable assets that are expiring this current year.|
|Asset requests|Count of hardware, consumable, and bundle requests in the catalog.|
|Asset lifecycle by state|Number of assets grouped by the lifecycle state such as Retired, In use, In stock.|
|Assets by model category|Number of assets grouped by the model category such as Software License, Consumable, Server.|
|Incomplete assets by model category|Asset models without purchase order number, purchase order line, or receiving line.|
|Spend by model category|Cost of assets grouped by their model category.|

## Load reports on Asset estate view

You can load charts or widgets that fetch a huge set of asset records on demand instead of loading them along with the page. This approach enables you to reduce the loading time for the Asset estate view.

The system property **sn\_itam\_workspace.asset\_estate\_enable\_lazy\_loading** provides you with an option to either selectively load reports you want to view or load reports concurrently with the page. By default, this system property is set to **False**. When this system property is enabled on your ServiceNow instance, you can view charts or widgets by using the **Load report** option.

![Load reports on Asset estate view](../../hardware-asset-management/image/asset-workspace-estate-load.png "Load reports on Asset estate view")

## Exclude Install Base Item \(IBI\) assets from reports

Any item that is provided as a service or sold to your customer is tracked as an Install Base Item \(IBI\). The Model category table associates Asset class, CI class, and Install Base Item \(IBI\) class.

By default, the reports and Important Actions in the Asset estate view include all the assets in the Asset \[alm\_asset\] table. However, you can filter IBI assets from reports and Important Actions cards. For details on configuration required to filter IBI assets, see the [Sold products exclusion from the reports and Important Actions of Asset Workspace \[KB1584331\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584331) article in the Now Support Knowledge Base

