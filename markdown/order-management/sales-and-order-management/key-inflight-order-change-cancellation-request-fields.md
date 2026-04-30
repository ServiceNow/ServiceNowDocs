---
title: Key inflight order change and cancellation request fields
description: Learn how the ServiceNow AI Platform uses key fields in the Customer Order and Order Line Item forms to track your order changes and cancellation requests. You can see how these fields operate and what information they show you when you revise or request a cancellation of an order, or order line items.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Inflight order changes, Order Management, Use, Sales Customer Relationship Management]
---

# Key inflight order change and cancellation request fields

Learn how the ServiceNow AI Platform uses key fields in the Customer Order and Order Line Item forms to track your order changes and cancellation requests. You can see how these fields operate and what information they show you when you revise or request a cancellation of an order, or order line items.

## Point of no return \(PONR\)

The **PONR** \(Point of No Return\) option on the Customer Order and Order Line item forms indicates the PONR state for the order or order line item. While fulfillment is in process, you can use the PONR option to determine if you can revise or request cancellation of an order or an order line item. You can only do these actions for orders and order line items that are in an In Progress state and have yet to reach the PONR stage.

**Note:** The **Revise Order** and **Cancel Order** buttons are enabled only for order or order line items in this state.

Learn what happens with the **PONR** option:

-   If you select the PONR option, it indicates that you can't revise or request a cancellation for the order or order line item while fulfillment is in progress. If any of the line items on an order reaches PONR, you can't revise the other line items on the same order.
-   If the check box is cleared, you can still revise or request a cancellation for the order or order line item.

**Note:** The **PONR** option is a system-assigned flag that you can't manually update.

By using the SET PONR action in Workflow Studio, your administrator can manually configure the PONR state in the fulfillment workflow. For example, in the demo data for the SD-WAN Edge product specification workflow, the PONR action is available after the Initiate CPE delivery task.

## Version

A customer or service order can go through multiple revisions during its fulfillment cycle. The **Version** field tracks the number of times that you revised or requested a cancellation of the order or order line item during the fulfillment process. A new order without any revisions has a version of 1 and automatically increments for each inflight revision.

## Revision Operation

The **Revision Operation** field indicates the type of revision operation, if any, that is taking place in the current version of the order or order line item. The types of revision are as follows:

-   **None**

    No update or cancellation is taking place for the order or order line item. This setting is the default for new orders and is applicable for orders without any Inflight revisions.

-   **Update**

    A Contact, Characteristic, Quantity, or Price inflight revision has been submitted for the order or order line item.

-   **Cancel**

    An order or order line item is canceled, or in the process of being canceled.


## Change Type

When you submit an inflight order revision, the ServiceNow AI Platform automatically assigns a change type for the tracking of the order changes that are submitted by users. Characteristic, Contact, or Price types are standard in the ServiceNow AI Platform.

The change types are automatically assigned to the order or order line item when an order fulfillment or service order agent makes the following types of changes.

<table id="table_bxg_ckg_fqb"><thead><tr><th>

Type of change made

</th><th>

Assigned change type

</th></tr></thead><tbody><tr><td>

Changes any of the order characteristics.

</td><td>

Characteristic

</td></tr><tr><td>

Adds, changes, or deletes the order contact information.

</td><td>

Contact

</td></tr><tr><td>

Changes any price field.

</td><td>

Price

</td></tr><tr><td>

Changes made to the order line item quantity for a product or service order.To learn more, see [Order quantity support in Order Management](order-quantity-support.md).

</td><td>

Quantity

</td></tr><tr><td>

Changes made to the order line item quantity for a product or service order due to the change in characteristic value.To learn more, see [Order quantity support in Order Management](order-quantity-support.md).

</td><td>

Quantity mapping characteristics

</td></tr><tr><td>

Changes made to the related order line items and related product inventory for a product or service order.

</td><td>

Related items

</td></tr></tbody>
</table>**Note:** Your administrator can also define additional change types for tracking purposes.

The related Inflight Order Line Item Changes \[sn\_ind\_tmt\_orm\_inflight\_order\_line\_item\_change\] table contains the following columns to track the revisions that were submitted for order line items.

<table id="table_hgd_pgg_fqb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order Line item

</td><td>

Identifier for the changed order line item.

</td></tr><tr><td>

Order Line version

</td><td>

Latest change version for the order line item. It tracks the number of times that you revised or requested a cancellation of the order line item during the fulfillment process.

</td></tr><tr><td>

Change Type

</td><td>

Type of change performed on the order line item.-   **Characteristic**

Change made to any of the characteristics on an existing order line item.

-   **Contact**

Changes made to the contact information on an existing order line item.

-   **Price**

Changes made to the pricing information on an existing order line item.

-   **Quantity**

Changes made to the order line item quantity for a product order.

-   **Other change types**

Additional change type that is defined by your administrator.


</td></tr><tr><td>

Updated by

</td><td>

Name of the person who updated the order line item.

</td></tr><tr><td>

Updated

</td><td>

Date and timestamp for the order line item change.

</td></tr></tbody>
</table>## State when initiating and approving inflight order revisions

When you initiate, and then approve, inflight order revisions, the affected order, order line items, domain orders, and order tasks go through different states.

When initiating an inflight order revision

To initiate an inflight order change, click **Revise Order** in the Customer Order form or in the Order Line Item form. The following actions take place:

1.  The customer or service order moves from an In Progress to a Revision in Progress state.
2.  The associated order line items move from an In Progress state to a Revision in Progress state.
3.  The associated product, service, and resource domain orders move from their current states to an On Hold state.
4.  The associated order tasks move to an On Hold state.

When approving an inflight order revision

To approve an inflight revision, an order fulfillment or service order manager clicks **Approve** in the Customer Order form. The following actions take place:

1.  The updated order and order line item information triggers the decomposition process as follows:
    -   The decomposition process may create additional domain product, service, and resource orders to incorporate the characteristic changes that were submitted as part of an inflight order change.
    -   It may also cancel existing domain orders that are not relevant to the requested change. For example, if a customer upgrades their purchased internet service to a higher speed, it would create a domain order for a modem that supports the higher speed service. It then would cancel the existing domain order for the modem that only supported lower speeds.
2.  The customer or service order moves from a Revision in Progress state to an Acknowledged state. When the order decomposition is complete, it then moves back to an In Process state.
3.  The associated order line items move from a Revision in Progress state to an Acknowledged state. When the order line item decomposition is complete, they then move back to an In Process state.
4.  The associated product, service, and resource domain orders change from an On Hold state to a Scheduled state. The associated subflows change the state again during fulfillment processing.

    New domain orders may also be created, based on the revisions that were submitted by the customers. They remain in either the Draft or the In Progress states, depending on the configuration of the fulfillment flow for the parent domain order.

5.  The ServiceNow AI Platform refreshes the fulfillment flows for all the decomposed orders. The ServiceNow AI Platform also reassesses all order tasks, depending on the sequencing of the tasks in the corresponding fulfillment workflow. The associated order tasks then move to one of the states that are listed in the following table:

    |State|Description|
    |-----|-----------|
    |Scheduled|An order task moves to this state and remains there until processed, as per the fulfillment workflow.|
    |In Progress|If an order task was in an In Progress state at the time you initiated the inflight order revision, it remains in this state. If the task requires a re-execution to perform a redo or undo action, it can also move from a Closed state to an In Process state.|
    |Closed Complete|If an order task was in a Closed Complete state at the time you initiated the inflight order revision, it stays in this state. It stays in this state as long as the task isn't in an inflight configuration due to other changes that were submitted as part of an inflight order revision.|

6.  After the order decomposition is complete and the fulfillment flow restarts, order fulfillment agents can go ahead and work on the associated order tasks to complete fulfillment.

## State when initiating and approving order cancellation requests

When you initiate and approve an order cancellation request, the affected order, order line items, domain orders, and order tasks go through different states during processing.

When initiating an order cancellation request

To initiate a cancellation request, you click **Cancel Order** in the Customer Order form, or **Cancel Order Line Item** in the Order Line Item form. The following actions take place:

1.  The order moves to an Assessing Cancellation state.
2.  The associated order line items move to an Assessing Cancellation state.
3.  The associated product, service, and resource domain orders move from their current states to an On Hold state.
4.  The associated order tasks move to an On Hold state.

When approving an order cancellation request

To approve an inflight revision or cancellation request, an order fulfillment or service order manager clicks **Approve** in the Customer Order form. The following actions take place:

1.  The decomposition process is triggered with the updated order and order line item information.
2.  The order moves from an Assessing Cancellation state to a Cancellation in Progress state.
3.  The associated order line items move to a Cancellation in Progress state.
4.  The associated domain product, service, and resource domain orders move from their current state to an On Hold state.
5.  The associated order tasks move to an On Hold state.

**Parent Topic:**[Managing inflight order changes and cancellation requests](inflight-order-change-mgt-overview.md)

