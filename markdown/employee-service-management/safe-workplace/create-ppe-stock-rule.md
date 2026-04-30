---
title: Create stock rules for PPE
description: Create a stock rule to automatically resupply a stockroom with an item.
locale: en-US
release: xanadu
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Workplace PPE Inventory Management, Workplace PPE Inventory Management, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create stock rules for PPE

Create a stock rule to automatically resupply a stockroom with an item.

## Before you begin

Role required: sn\_imt\_ppe.ppe\_admin

## About this task

When an item drops below a specified quantity, the stock rule automatically creates a transfer order. The transfer order resupplies the stockroom by transferring the required items from another stockroom. For more information about transfer orders, see [Transfer orders](https://www.servicenow.com/docs/access?context=transfer-orders-asset&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **PPE Inventory Management** &gt; **Inventory** &gt; **Stock Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Model|The product model for the rule.|
    |Threshold|The item quantity that triggers a restock. For example, enter a threshold of 150 for masks that should be restocked when inventory drops below 150 in the specified stockroom.|
    |Restocking option|Stockroom. This value is automatically populated.|
    |Parent stockroom|The stockroom that the new items are transferred from.|
    |Active|When selected, the rule is active and items are automatically restocked. When cleared, the rule is not active and items are not automatically restocked.|
    |Stockroom|The stockroom that you want to be automatically restocked by the rule.|
    |Order size|The number of new items to order for the stockroom.|

4.  Click **Submit**.


**Parent Topic:**[Set up Workplace PPE Inventory Management](set-up-ppe.md)

**Previous topic:**[Reduce PPE stock](reduce-ppe-stock.md)

**Next topic:**[PPE Inventory Overview dashboard](../concept/ppe-overview-dashboard.md)

