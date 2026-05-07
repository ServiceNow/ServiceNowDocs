---
title: Purchase order
description: A purchase order is a binding contract between a buyer and a supplier that authorizes a purchasing transaction. It contains the descriptions, quantities, prices, applicable discounts, payment terms, delivery dates, and other associated terms and conditions with the supplier.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase order

A purchase order is a binding contract between a buyer and a supplier that authorizes a purchasing transaction. It contains the descriptions, quantities, prices, applicable discounts, payment terms, delivery dates, and other associated terms and conditions with the supplier.

In a purchase order, the key fields are the following:

<table id="table_myc_ln5_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the purchase order for a supplier product.

</td></tr><tr><td>

Number

</td><td>

System-generated unique identifier of the purchase order.

</td></tr><tr><td>

ERP number

</td><td>

The purchase order number that is synced from ERP systems.

</td></tr><tr><td>

Version

</td><td>

The version of the purchase order. A revised purchase order has a higher version number.

</td></tr><tr><td>

Business owner

</td><td>

The user who placed the order.

</td></tr><tr><td>

Status

</td><td>

Status of the purchase order.

</td></tr><tr><td>

Purchase requisition

</td><td>

The purchase requisition associated with this order.

</td></tr><tr><td>

Primary contact

</td><td>

Person within the procurement team who can be contacted with questions about the order. This field is populated or updated with the same user in the **Assigned to** field on the purchase requisition.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Supplier

</td><td>

Supplier who provides the product of this order.

</td></tr><tr><td>

Order type

</td><td>

Indicates if the purchase order is of the type **Standard** or **Blanket**.

</td></tr><tr><td>

Minimum spend

</td><td>

Minimum amount that must be spent to avail a discount.This field isn’t displayed for a blanket order type.

</td></tr><tr><td>

Discount percentage

</td><td>

Discount provided if the minimum spend requirement is met.This field isn’t displayed for a blanket order type.

</td></tr><tr><td>

Total amount

</td><td>

The total cost of purchase requisition calculated as the sum from all related purchase lines.

</td></tr><tr><td>

Released amount

</td><td>

The budget that is consumed so far.This field is visible for blanket order type.

</td></tr><tr><td>

Shipping method

</td><td>

Details of the carrier, the applicable suppliers, and the valid delivery location countries for those suppliers.For more information on shipping methods and handling fees, see [Handling fees](../concept/handling-fees.md).

</td></tr><tr><td class="sub-head" colspan="2">

Accounting Details

</td></tr><tr><td>

Cost center

</td><td>

The cost center incurring the expense of this order.This field is carried over from the related purchase requisition.

</td></tr><tr><td>

Legal entity

</td><td>

Internal legal entity making this purchase.This field is carried over from the related purchase requisition.

</td></tr><tr><td>

Purchasing entity

</td><td>

The organizational entity associated with the business owner making this purchase.This field is carried over from the related purchase requisition.

</td></tr><tr><td>

Payment term

</td><td>

The agreed time and conditions of payment to the supplier.

</td></tr><tr><td>

Received amount

</td><td>

Indicates if the order is partially or fully delivered. This value is the sum of the receipt values in the child purchase order lines.This field is visible for standard order type.

</td></tr><tr><td>

Received percent

</td><td>

Indicates if the order is partially or fully delivered. This value is the sum of the receipt values in the child purchase order lines.This field is visible for standard order type.

</td></tr><tr><td>

Invoiced amount

</td><td>

Amount invoiced for the product ordered. While other charges are added to the amount invoiced, discount amount is subtracted from it.This field is visible for standard order type.

</td></tr><tr><td>

Amount paid

</td><td>

Amount paid for the product ordered.This field is visible for standard order type.

</td></tr><tr><td>

Remaining balance

</td><td>

Amount due to the supplier for the order.This field is visible for standard order type.

</td></tr></tbody>
</table>During purchase order integration, any attachments with valid sys-ids are copied from the Inbound Purchase Order staging table record to this Purchase Order primary table record. This is done through a transform script, which is part of the Order stage transform map, triggered onAfter. Go to the purchase order record on the Purchase Order table based on the ERP number and purchase order number, and verify that your attachments are present on the target record. You can delete or rename attachments as needed, without creating duplicates.

The receipt fields \(**Received amount** and **Received percent**\) on the Accounting Details section of a purchase order are summations of the receipt fields on the child purchase order lines, which are populated based on the following conditions:

-   For purchase order line of goods:
    -   When goods have been received: The received quantity is populated when a receipt is created. The received amount and received percent are calculated based on the received quantity.
    -   When goods haven’t been received: The received amount is populated with the line amount invoiced \(editable field\) when the status of the invoice line associated with the purchase order line is Invoice Confirmed. The received quantity and received percent are calculated based on the received amount.
-   For purchase order line of services:

    **Note:** Business rules pertaining to handling state changes, handling tax and charges, default invoice fields, populating invoice line amounts, handling line total changes, and populating supplier products are available only if you haven't installed the Shopping Hub plugin and are still using the Source-to-Pay Common Architecture plugin.​

    -   When the acknowledgment type is milestones:
        -   If the milestone payout is amount, the received amount is populated accordingly. The received quantity and received percent are calculated based on the received amount.
        -   If the milestone payout is a percentage, the received percent is populated accordingly. The received quantity and received amount are calculated based on the received percent.
    -   When the acknowledgment type is service acknowledgment: The received amount is populated based on the approved invoice line amount. The received quantity and received percent are calculated based on the received amount.
    -   When the acknowledgment type is a two-way match: The received amount is populated with the line amount invoiced \(editable field\) when the status of the invoice line associated with the purchase order line is Invoice Confirmed. The received quantity and received percent are calculated based on the received amount.

For more information on purchase order lines, see [Purchase order lines](../../accounts-payable-operations/reference/purchase-order-lines.md).

The following are the key related lists of a purchase order record:

<table id="table_nss_z45_flb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase Order Lines

</td><td>

Lists the standard purchase order releases for a blanket purchase order.​

</td></tr><tr><td>

Approval Plans

</td><td>

Displays all the approval plans created against this purchase order.

</td></tr><tr><td>

Receipts

</td><td>

Provides details of the receipts created for this purchase order. For details, see [Receipts](receipts.md).This related list is visible for standard order type.

</td></tr><tr><td>

Milestones

</td><td>

Provides details of the milestones for this purchase order. For details, see [Milestones](milestones.md).This related list is visible for standard order type.

</td></tr><tr><td>

Invoices

</td><td>

Provides details of the invoices generated for this purchase order. For details, see [Invoices](invoices.md).This related list is visible for standard order type.

</td></tr><tr><td>

Related Contracts

</td><td>

Provides details of related contracts associated for this purchase order. For details, see [Contracts](contracts.md).This related list is visible for standard order type.

</td></tr><tr><td>

Purchasing Permission

</td><td>

Carried over from the related purchase requisition.This related list is visible for blanket order type.

</td></tr><tr><td>

Purchase Order Releases

</td><td>

This related list is visible for blanket order type.

</td></tr><tr><td>

Purchasing Tasks

</td><td>

Provides information of tasks for this purchase order.

</td></tr><tr><td>

Purchase Order History

</td><td>

List of purchase orders before the current revision. This related list is visible if the purchase order has revisions.

</td></tr></tbody>
</table>For a list of all purchase order states and the conditions that trigger each state change, see [Purchase requisition, purchase order, and sourcing request states](pr-po-sr-states.md).

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

