---
title: Create a purchase order
description: You can create a purchase order. Purchase orders specify assets to order from a single vendor.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Procurement purchase order management for assets, Procurement, IT Asset Management]
---

# Create a purchase order

You can create a purchase order. Purchase orders specify assets to order from a single vendor.

## Before you begin

Role required: procurement\_admin or procurement\_user

## About this task

For example, an organization can create a purchase order to buy 20 laptop computers or 10 servers. Information on a purchase order enables physical and financial tracking of the assets that were ordered.

You can also use a transfer order if an asset is already owned by an organization. A transfer order is used to internally transfer assets from one stockroom to another instead of purchasing the assets. For example, a company stockroom in New York has five laptops that are needed in Boston. You create a transfer order to move the laptops from the New York stockroom to the Boston stockroom.

After you create a purchase order, the **Receiving Slip** related list is available on the Purchase Order form. A receiving slip is created manually or automatically when the item is received. The **Receiving Slip** related list shows all receiving slips related to the purchase order. After a receiving slip is added to a purchase order, all fields on the purchase order record become read-only.

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Orders** &gt; **Purchase Orders**.

2.  Click **New**.

3.  Complete the form.

<table id="id_tjv_lqc_xwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The unique number identifying the purchase order.

</td></tr><tr><td>

Due by

</td><td>

The date by which the purchase order **Total cost** must be paid.

</td></tr><tr><td>

Vendor

</td><td>

The supplier to which the purchase order was issued.

</td></tr><tr><td>

Ship to

</td><td>

The stockroom to which the items on the purchase order should be shipped.**Note:** This field is required but doesn't affect creating requisitions for software on Coupa.

</td></tr><tr><td>

PO date

</td><td>

The date on which the purchase order was created.

</td></tr><tr><td>

Status

</td><td>

The status of the purchase order: **Canceled**, **Ordered**, **Received**, **Requested**, or **Suspended**.

</td></tr><tr><td>

Assigned to

</td><td>

The user to whom the purchase order is assigned.

</td></tr><tr><td>

Bill to

</td><td>

The location responsible for paying the purchase order **Total cost**.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the purchase order.

</td></tr><tr><td class="sub-head" colspan="2">

General section

</td></tr><tr><td>

Shipping

</td><td>

The delivery method to be used when shipping the items on the purchase order.

</td></tr><tr><td>

Terms

</td><td>

The purchase order payment terms: **Credit**, **Net 30 days**, or **Net 90 days**.

</td></tr><tr><td>

Ship rate

</td><td>

The amount that must be paid for the delivery method specified in the **Shipping** field.

</td></tr><tr><td>

Total cost

</td><td>

The sum of all item costs on the purchase order and the shipping costs.

</td></tr><tr><td>

Description

</td><td>

A full description of the purchase order contents.

</td></tr><tr><td class="sub-head" colspan="2">

Details section

</td></tr><tr><td>

Initial request

</td><td>

The record number of the request that requires the items on the purchase order.

</td></tr><tr><td>

Requested by

</td><td>

The user requesting the items on the purchase order.**Note:**

The email ID or email address of the user requesting the items on the purchase order must be the same on both Coupa and ServiceNow ServiceNow application.

</td></tr><tr><td>

Requested

</td><td>

The date the user in the **Requested by** field requested the items on the purchase order.

</td></tr><tr><td>

Ordered

</td><td>

The date and time of clicking the **Order** button on the Purchase Order form.

</td></tr><tr><td>

Expected delivery

</td><td>

The date the items associated with the purchase order are expected to arrive in the stockroom identified in the **Ship to** field. This field can’t be edited when the purchase order has a **Status** of **Received** or **Canceled**. \(For more information about this field, see[Purchase order expected delivery date](../reference/r_SetExpectDelDateOnPurchOrder.md).\)

</td></tr><tr><td>

Received

</td><td>

The date and time at which the purchase order status changed to **Received**.

</td></tr><tr><td>

Contract

</td><td>

The record number of the contract with the vendor from which the items on the purchase order are ordered.

</td></tr><tr><td>

Department

</td><td>

The department responsible for paying for the purchase order.

</td></tr><tr><td>

Budget number

</td><td>

The budget number related with the purchase order.

</td></tr><tr><td>

Vendor account

</td><td>

The vendor account related with the purchase order.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Add purchase order line items to specify what you are ordering from this vendor.

-   **[Create a purchase order line item](t_CreateAPurchaseOrderLineItem.md)**  
After you save a new purchase order, you create purchase order line item records to specify the individual items to order.
-   **[Purchase order status](../reference/r_FollowAPurchaseOrderStatus.md)**  
Purchase orders follow a specific life cycle. The **Status** field on the purchase order record is always read-only.
-   **[Purchase order expected delivery date](../reference/r_SetExpectDelDateOnPurchOrder.md)**  
The purchase order record and the purchase order line item record both contain the **Expected delivery** date field.
-   **[Cancel a purchase order](t_CancelAPurchaseOrder.md)**  
You can cancel purchase orders with a status of **Requested**, **Ordered**, or **Pending Delivery**.
-   **[Cancel a purchase order line item](t_CancelAPurchaseOrderLineItem.md)**  
You can cancel a purchase order line items with a status of **Requested**, **Ordered**, or **Pending Delivery**.
-   **[Reorder a purchase order](t_ReorderAPurchaseOrder.md)**  
You can reorder a purchase order that was canceled.
-   **[Reorder a purchase order line item](t_ReorderAPurchaseOrderLineItem.md)**  
You can reorder a purchase order line item that was canceled.

**Parent Topic:**[Procurement purchase order management for assets](../concept/c_UseProcurement.md)

**Related topics**  


[Consumable assets](../concept/c_ReceiveAConsumableAsset.md)

[Track a request from the service catalog](t_TrackReqFromServiceCatalog.md)

[Cancel a request from the service catalog](t_CancelReqFromServCatalog.md)

[View and edit a catalog task](t_ViewAndEditACatalogTask.md)

[Create an asset and reserve it for the requester](t_CreateAssetReserveForRequester.md)

[Manage transfer orders](https://www.servicenow.com/docs/access?context=c_TransferOrders&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)

