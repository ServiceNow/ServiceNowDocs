---
title: Create a stockroom type
description: If you need stockroom types that are not included in the base system, you can create a custom stockroom type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/t\_CreateANewStockroomType.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure stockrooms, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Create a stockroom type

If you need stockroom types that are not included in the base system, you can create a custom stockroom type.

## Before you begin

Role required: inventory\_admin

## About this task

Check the [priority level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/r_StockroomTypes.md) of the stockroom types provided in the base instance to ensure that you assign the correct priority level to any new stockroom types you create. You can also modify the stockroom types included in the base system.

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Stock** &gt; **Stockroom Types** and create a record \(see table for field descriptions\).

    |Field|Description|
    |-----|-----------|
    |Name|Display name of the stockroom type.|
    |Description|General information about the stockroom type.|
    |External stockroom|Whether stockrooms of this type are managed internally \(check box cleared\) or managed externally by a third party \(check box selected\).|
    |Priority|Level of precedence for this type of stockroom.|
    |Shipment required|Option that determines if stockrooms of this type require shipment by default.|
    |Value|Internal identifier of the stockroom type.|

2.  Select **Submit**.


**Parent Topic:**[Configure stockrooms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/configure-stockrooms-ham.md)

