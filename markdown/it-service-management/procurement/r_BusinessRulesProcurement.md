---
title: Business rules installed with Procurement
description: Procurement plugin adds the following business rules.
locale: en-US
release: yokohama
product: Procurement
classification: procurement
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Components installed with Procurement, Activate Procurement, Procurement, Asset Management, IT Service Management]
---

# Business rules installed with Procurement

Procurement plugin adds the following business rules.

<table id="table_zgd_3vv_dp"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Adjust remaining quantity

</td><td>

Purchase order line items \[proc\_po\_item\]

</td><td>

Calculates the remaining quantity of items ordered on a purchase order line items by subtracting the amount received from the amount ordered.

</td></tr><tr><td>

Can request be sourced

</td><td>

Request \[sc\_request\]

</td><td>

Checks if a request can be sourced.

</td></tr><tr><td>

Cancel Procurement Orders

</td><td>

Request \[sc\_request\]

</td><td>

Cancels all unreceived purchase orders and unshipped transfer order lines associated with the request's items if the request state changes to **Closed Cancelled**.

</td></tr><tr><td>

Check if req item is sourced

</td><td>

Requested Item \[sc\_req\_item\]

</td><td>

Sets the **Sourced** field on the parent request to **true** if all requested items have been sourced.

</td></tr><tr><td>

Check if request is sourceable

</td><td>

Requested Item \[sc\_req\_item\]

</td><td>

Checks if the request associated with a requested item can be sourced \(obtained from a transfer order or by creating a purchase order to a vendor\).

</td></tr><tr><td>

Create Assets

</td><td>

Receiving Slip Line \[proc\_rec\_slip\_item\]

</td><td>

If the purchase order line item is available, creates the assets for a receiving slip line when the slip line assets are received.

</td></tr><tr><td>

Handle roll up states and assets removal

</td><td>

Purchase order line items \[proc\_po\_item\]

</td><td>

Manages purchase order line items if they are canceled or received. If a purchase order line is canceled, this business rule deletes any pre-created assets. This business rule also checks the status of other purchase order lines that share the same purchase order and, if necessary, updates the status of the purchase order. For example, when the last purchase order line is received, the status of the purchase order changes to **Received**.

</td></tr><tr><td>

Redirect TOL to existing TO-Procurement

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

Attaches a transfer order line to an existing transfer order if the transfer order is in the **Draft** stage and has the same **From stockroom** and **To stockroom** values as the transfer order line.

</td></tr><tr><td>

Shipping Cost Changes

</td><td>

Purchase Order \[proc\_po\]

</td><td>

Recalculates the total cost of the purchase order if the shipping rate changes.

</td></tr><tr><td>

State Change

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

Marks the requested item as **Received** if the state of the associated transfer order line changes to **Received**.

</td></tr><tr><td>

State Change

</td><td>

Purchase order line items \[proc\_po\_item\]

</td><td>

Sets the time at which the purchase order line item is ordered and updates the original requested item when the purchase order line item is received.

</td></tr><tr><td>

State Change PO

</td><td>

Purchase Order \[proc\_po\]

</td><td>

Changes the purchase order line item status when the status of the associated purchase order changes.

</td></tr><tr><td>

Total Cost

</td><td>

Purchase order line items \[proc\_po\_item\]

</td><td>

Calculates the total order cost based on the cost of individual items and the quantity ordered. When you receive a purchase order line item, this business rule also takes the following steps.-   Populates the **List price** field with the value from the **Cost** field unless you enter a different value.
-   Calculates the **Total list price** field value by multiplying the **List price** and **Ordered quantity** values.

</td></tr><tr><td>

Update expected delivery date for PO

</td><td>

Purchase order line items \[proc\_po\_item\]

</td><td>

Sets the **Expected delivery date** for purchase orders to the latest purchase order line **Expected delivery date**.

</td></tr><tr><td>

Update expected delivery date for POLs

</td><td>

Purchase Order \[proc\_po\]

</td><td>

Sets the **Expected delivery date** of associated purchase order lines to the purchase order's **Expected delivery date** if at least one of the following conditions is true.-   The purchase order line has no expected delivery date.
-   The purchase order line's expected delivery date is later than the purchase order's expected delivery date.
-   The purchase order line's expected delivery date is the same as the purchase order's previous delivery date.

</td></tr><tr><td>

Update Ordered Date

</td><td>

Purchase Order \[proc\_po\]

</td><td>

Sets the **Ordered date** field to the date and time at which the status of the purchase order is set to **Ordered**.

</td></tr><tr><td>

Update PO

</td><td>

Purchase order line items \[proc\_po\_item\]

</td><td>

Updates the purchase order if the cost of any purchase order line item changes.

</td></tr><tr><td>

Update Purchase Order Line

</td><td>

Receiving Slip Line \[proc\_rec\_slip\_item\]

</td><td>

Updates the **Quantity received** field on the associated purchase order line item when a receiving slip item is received.

</td></tr><tr><td>

Update Request Item CI

</td><td>

Hardware \[alm\_hardware\]

</td><td>

Sets the **Configuration item** field on the catalog task and requested item to the related hardware CI created during the procurement process.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Procurement](r_InstalledWithProcurement.md)

**Related topics**  


[Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

