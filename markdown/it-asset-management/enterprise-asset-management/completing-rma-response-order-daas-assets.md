---
title: Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets
description: After you create an RMA response order with corresponding RMA response order lines, you must perform various tasks to complete and close the order.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-10-23"
reading_time_minutes: 8
breadcrumb: [Managing RMA response orders for defective DaaS assets, Enterprise Asset Management for Providers, Enterprise Asset Management, IT Asset Management]
---

# Completing a Return Merchandise Authorization \(RMA\) response order for defective Device as a Service \(DaaS\) assets

After you create an RMA response order with corresponding RMA response order lines, you must perform various tasks to complete and close the order.

Based on the action that you want to take on your defective DaaS assets, you must complete a specific set of tasks for each RMA response order line within an RMA response order. After you complete all tasks for an order line, it moves to the Completed stage. After every order line reaches the Completed stage, the order is closed.

<table id="table_anw_fyn_bhc"><thead><tr><th>

Supported RMA action

</th><th>

Tasks

</th></tr></thead><tbody><tr><td>

On-site repair

</td><td>

1.  [RMA assessment task to assess the defective DaaS asset](../task/assess-daas-asset-rma-response-order.md).
2.  [Schedule task to schedule a visit to the customer site](../task/schedule-customer-visit-rma-response-order.md).
3.  [Evaluate RMA asset task to evaluate the defective DaaS asset](../task/evaluate-daas-asset-rma-response-order.md).
4.  [Repair asset task to repair the defective DaaS asset](../task/repair-daas-asset-rma-response-order.md).
5.  [Evaluate asset task to evaluate the repaired DaaS asset](../task/evaluate-repaired-daas-asset-rma-response-order.md).
6.  The customer redeploys or [disposes of](../task/create-eamdisposal-order.md) the repaired DaaS asset.

</td></tr><tr><td>

On-site replacement

</td><td>

1.  [RMA assessment task to assess the defective DaaS asset](../task/assess-daas-asset-rma-response-order.md).
2.  [Schedule task to schedule a visit to the customer site](../task/schedule-customer-visit-rma-response-order.md).
3.  [Evaluate RMA asset task to evaluate the defective DaaS asset](../task/evaluate-daas-asset-rma-response-order.md).
4.  [Ship task to have the customer ship the defective DaaS asset to you](../task/ship-daas-asset-rma-response-order.md).
5.  [Receive asset task to verify that you received the defective DaaS asset from the customer](../task/receive-shipped-daas-asset-rma-response-order.md).
6.  [Complete an inbound asset order to provide the customer with a new DaaS asset](completing-inbound-asset-order-daas-assets.md).

</td></tr><tr><td>

Off-site repair

</td><td>

1.  [RMA assessment task to assess the defective DaaS asset](../task/assess-daas-asset-rma-response-order.md).
2.  [Ship task to have the customer ship the defective DaaS asset to you](../task/ship-daas-asset-rma-response-order.md).
3.  [Receive asset task to verify that you received the defective DaaS asset from the customer](../task/receive-shipped-daas-asset-rma-response-order.md).
4.  [Evaluate RMA asset task to evaluate the defective DaaS asset](../task/evaluate-daas-asset-rma-response-order.md).
5.  [Repair asset task to repair the defective DaaS asset](../task/repair-daas-asset-rma-response-order.md).
6.  [Evaluate asset task to evaluate the repaired DaaS asset](../task/evaluate-repaired-daas-asset-rma-response-order.md).
7.  [Ship task to ship the repaired DaaS asset back to the customer](../task/ship-daas-asset-rma-response-order.md).
8.  [Receive asset task to verify that the customer received the repaired DaaS asset](../task/receive-shipped-daas-asset-rma-response-order.md).
9.  The customer redeploys or [disposes of](../task/create-eamdisposal-order.md) the repaired DaaS asset.

</td></tr><tr><td>

Off-site replacement

</td><td>

1.  [RMA assessment task to assess the defective DaaS asset](../task/assess-daas-asset-rma-response-order.md).
2.  [Ship task to have the customer ship the defective DaaS asset to you](../task/ship-daas-asset-rma-response-order.md).
3.  [Receive asset task to verify that you received the defective DaaS asset from the customer](../task/receive-shipped-daas-asset-rma-response-order.md).
4.  [Evaluate RMA asset task to evaluate the defective DaaS asset](../task/evaluate-daas-asset-rma-response-order.md).
5.  [Complete an inbound asset order to provide the customer with a new DaaS asset](completing-inbound-asset-order-daas-assets.md).

</td></tr></tbody>
</table>-   **[Complete the RMA assessment task for a defective Device as a Service DaaS asset](../task/assess-daas-asset-rma-response-order.md)**  
Complete the RMA assessment task for a defective DaaS asset by assessing the asset and determining the action that you want to take on it. You can choose to repair it, replace it, or reject the associated RMA request.
-   **[Complete the Schedule task for a defective Device as a Service DaaS asset](../task/schedule-customer-visit-rma-response-order.md)**  
If you want to perform an on-site repair or replacement for a defective DaaS asset, complete the Schedule task for the asset by scheduling a visit to the customer site.
-   **[Complete the Evaluate RMA asset task for a defective Device as a Service DaaS asset](../task/evaluate-daas-asset-rma-response-order.md)**  
Complete the Evaluate RMA asset task for a defective DaaS asset by evaluating the asset and determining whether you want to repair or replace it.
-   **[Complete the Repair asset task for a defective Device as a Service DaaS asset](../task/repair-daas-asset-rma-response-order.md)**  
Complete the Repair asset task for a defective DaaS asset by repairing the asset either on-site or off-site.
-   **[Complete the Evaluate asset task for a defective Device as a Service DaaS asset](../task/evaluate-repaired-daas-asset-rma-response-order.md)**  
After you repair a defective DaaS asset, complete the Evaluate asset task by evaluating the asset and determining if it can be redeployed.
-   **[Complete the Ship task for a defective Device as a Service DaaS asset](../task/ship-daas-asset-rma-response-order.md)**  
If you want to perform a replacement or an off-site repair for a defective DaaS asset, you must complete the associated Ship task by having the customer ship the asset to you. If you choose to repair the asset, you must complete the associated Ship task by shipping the asset back to the customer after a successful repair.
-   **[Complete the Receive asset task for a defective Device as a Service DaaS asset](../task/receive-shipped-daas-asset-rma-response-order.md)**  
After a customer ships a defective DaaS asset to you for repair or replacement, or after you ship a repaired DaaS asset back to a customer, complete the Receive asset task by verifying that the asset was received successfully.

**Parent Topic:**[Managing Return Merchandise Authorization \(RMA\) response orders for defective Device as a Service \(DaaS\) assets](managing-rma-response-orders-daas-assets.md)

