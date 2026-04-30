---
title: Create a requisition on Coupa through Procurement application
description: Create software requisitions directly on Coupa through the ServiceNow Procurement application to purchase software.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Integrating with Coupa, Integrating with external procurement applications, Procurement, Asset Management, IT Service Management]
---

# Create a requisition on Coupa through Procurement application

Create software requisitions directly on Coupa through the ServiceNow Procurement application to purchase software.

## Before you begin

To create a requisition on Coupa through ServiceNow Procurement application, you must perform the following tasks.

-   Create and publish a Coupa integration profile. For more information see, [Create a Coupa integration profile](create-coupa-int-profile.md).
-   Ensure that the Purchase Order you create has at least one Purchase Order Line, and all Purchase Order Lines must be for software products.
-   Synchronize reference data types on both ServiceNow Procurement and Coupa applications. For more information, see [Reference data synchronization](../reference/ref-data-coupa.md).

If all these conditions are met, you can create a requisition in Coupa.

If the conditions aren’t met, requisitions aren't created on Coupa, and the legacy procurement flow continues on the Procurement application.

Role required: sam\_admin and procurement\_integrator

**Note:** The procurement\_integrator role is added to the sam\_admin role. The procurement\_integrator role enables the SAM admin to view the connections and aliases.

## About this task

You can create a requisition on Coupa through the following ways:

-   When a user requests software through Service Catalog. For more information, see [Request a catalog item from Service Portal](https://www.servicenow.com/docs/access?context=request-cat-item-portal&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   If a procurement\_user or sam\_admin directly creates a Purchase Order on the Procurement application. For more information, see [Create a Purchase Order](t_CreateAPurchaseOrder.md).
-   When a sam\_user creates a Purchase Order directly from the Remediation Options form. For more information, see [View software model results](https://www.servicenow.com/docs/access?context=t_ViewSWModelResults&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

Requisitions are of the following types:

-   **Catalog request**: A requisition created for an item that is already present in the external purchasing application.
-   **Non catalog request**: A requisition created for an item that isn't present in the product catalog of the organization.

For more information about creating a Purchase Order, see [Create a purchase order](t_CreateAPurchaseOrder.md).

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Orders** &gt; **Purchase Orders**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="id_axh_3cb_gxb"><thead><tr><th>

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

The date the items associated with the purchase order are expected to arrive in the stockroom identified in the **Ship to** field. This field can’t be edited when the purchase order has a **Status** of **Received** or **Canceled**. \(For more information about this field, see[Purchase order expected delivery date](https://www.servicenow.com/docs/access?context=r_SetExpectDelDateOnPurchOrder&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).\)

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
</table>4.  Right-click on the form and select **Save**.

    You can add purchase order line items to specify what you are ordering from this vendor. For more information about creating a purchase order line item, see [Create a purchase order line item](t_CreateAPurchaseOrderLineItem.md). A requisition line is created with a unique ID in Coupa.

5.  After you’ve added at least one purchase order line item, select **Order**.

    A requisition ID is displayed on your Purchase Order and the corresponding requisition line IDs are displayed on your Purchase Order Lines.

    **Note:** Wait for some time and then reload the Purchase Order form to view the generated IDs or errors.


## Result

After the status of the Purchase Order is **Received** on Coupa, the following activities occur:

-   **Assets** and **Receiving Slips** get created and you can find the **Purchase Order Number** on the Purchase Order form.
-   The Asset Management - Procurement Integration application automatically generates entitlements.
-   On receipt of the assets, the scheduled job **ITAM - Sync Coupa purchase orders** creates a Receiving Slip and Receiving Slip Lines on the ServiceNow Procurement application. This job also pulls the Coupa fields such as Manufacturer part number, Status, and Receiving quantity. The values returned from Coupa through the receiving transactions are used to populate the created entitlements. However, if these values are not available from the receiving slips, then the Asset Management - Procurement Integration application uses the values populated in the Purchase Order of the Procurement application.
-   If any discrepancy exists on the Purchase Order, Asset Management - Procurement Integration creates entitlement import errors. You can view the errors by selecting the **Entitlement Import Errors** tab under a Purchase Order, Purchase Order Line item, and Receiving Slip line.

