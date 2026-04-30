---
title: Remove enterprise assets from a move order
description: Remove any enterprise assets that you no longer want to include in a move order.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing enterprise asset move orders, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Remove enterprise assets from a move order

Remove any enterprise assets that you no longer want to include in a move order.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, navigate to **Asset operations** &gt; **Moves** &gt; **Move orders**.

2.  From the list of available move orders, select the move order that you want to remove enterprise assets from.

    The move order record opens.

3.  On the move order record, select the **Enterprise move lines** tab.

4.  From the list of enterprise move lines, select the check box for every enterprise asset that you want to remove.

    **Note:** Each enterprise move line corresponds with a specific enterprise asset.

    **Note:** If you select an enterprise asset that contains any child assets, all child assets are also removed from the move order.

5.  Select **Remove**.


## Result

The selected enterprise assets are automatically updated with a status of Cancelled. All enterprise move tasks that are associated with the corresponding enterprise move lines are also updated with a state of Closed Incomplete.

**Parent Topic:**[Managing enterprise asset move orders](../concept/managing-enterprise-asset-move-orders.md)

