---
title: Close transfer order line task
description: Progress a transfer order line through diffident stages by closing the transfer order line task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/asset-management/move-transfer-order-line-through-stages.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-04-19"
reading_time_minutes: 1
breadcrumb: [Transfer order tasks, Manage transfer order, Use, Asset Management, IT Asset Management]
---

# Close transfer order line task

Progress a transfer order line through diffident stages by closing the transfer order line task.

## Before you begin

Role required: inventory\_user

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Orders** and open the transfer order.

2.  In the Transfer Order Lines related list, open the transfer order line.

3.  In the Transfer Order Line Tasks related list, open the current open task.

    The task name reflects the current stage, for example, **Ready for fulfillment**.

4.  Review the task details and select **Close Task**.


## Result

-   The current task closes with a status of Closed Complete.
-   The next task in the sequence opens automatically.
-   he asset status on the asset record updates to reflect the new stage.

## What to do next

Keep closing each task until you reach the last stage **Received**. After you close the task for the **Received** stage, the transfer order line is completed and closed. All transfer order lines and the transfer order are marked **Delivered**.

**Parent Topic:**[Transfer order tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/work-with-transfer-orders.md)

**Related topics**  


[Create a transfer order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/create-a-transfer-order.md)

[Create transfer order line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/create-transfer-order-line.md)

[Summary of transfer order line tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-management/r_SummaryOfTransferOrderStages.md)

