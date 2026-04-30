---
title: Requesting a Return Merchandise Authorization \(RMA\) for defective enterprise assets
description: A Return Merchandise Authorization \(RMA\) is an agreement between a buyer and a seller that allows the buyer to return, replace, or request the repair of a defective product within the specified warranty period. With the Enterprise Asset Management application, you can submit RMA orders to either replace or repair your defective enterprise assets.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Requesting a Return Merchandise Authorization \(RMA\) for defective enterprise assets

A Return Merchandise Authorization \(RMA\) is an agreement between a buyer and a seller that allows the buyer to return, replace, or request the repair of a defective product within the specified warranty period. With the Enterprise Asset Management application, you can submit RMA orders to either replace or repair your defective enterprise assets.

## Return Merchandise Authorization flow

When you submit an RMA order for your defective enterprise assets, the Enterprise Asset Management application automatically generates an RMA order line for each defective enterprise asset that was added to the order. You can then use these RMA order lines to track and manage the RMA process for each of those enterprise assets separately.

**Note:** You can submit RMA orders for serialized enterprise assets only.

For every RMA order line within an RMA order, you must complete a Prepare task to indicate how you want to proceed with the RMA process for the given enterprise asset. Based on the terms that you agreed upon with the asset vendor, you can choose to

-   complete the RMA process on-site,
-   complete the RMA process off-site with the asset vendor,
-   or reject the RMA for the given enterprise asset.

If you choose to complete the RMA process on-site, the defective enterprise asset can only be repaired. You must complete all necessary on-site repair tasks to move the corresponding RMA order line to the Completed stage. If you choose to complete the RMA process off-site with the asset vendor, the defective enterprise asset can either be replaced or repaired. You must work with the asset vendor to complete all necessary off-site replacement or repair tasks so that you can move the corresponding RMA order line to the Completed stage. If you choose to reject the RMA, the RMA order line automatically moves to the Completed stage without requiring any further action. After every RMA order line within an RMA order reaches the Completed stage, the order is closed.

## Return Merchandise Authorization cancellations

If you have not completed the Prepare task for any of the RMA order lines within an RMA order, you can cancel the entire RMA order. After the order is canceled, all associated RMA order lines and tasks are also canceled.

-   **[Submit a Return Merchandise Authorization \(RMA\) order for your defective enterprise assets](../task/submit-rma-order.md)**  
Submit a Return Merchandise Authorization \(RMA\) order to initiate the replacement or repair of your defective enterprise assets.
-   **[Closing a Return Merchandise Authorization \(RMA\) order for your defective enterprise assets](closing-rma-order.md)**  
After you submit a Return Merchandise Authorization \(RMA\) order for your defective enterprise assets, you must complete various tasks to close the order.

**Parent Topic:**[Create and manage enterprise asset inventory](managing-enterprise-asset-inventory.md)

