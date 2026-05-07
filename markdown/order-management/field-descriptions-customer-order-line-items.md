---
title: Customer and service order line items forms
description: The Order Line Items form enables you to select, review, and modify the captured customer or service order line items.The order line items form line item details section enables you to review and modify general details for a customer or service order line item.The Order Line Items form - dates section enables you to review and modify crucial date details for a customer order line item.The Order Line Items form - shipping address details section enables you to review and modify the shipping details for a customer order line item.The Order Line Items form - notes section enables you to review and modify the additional details for a customer order line item.The Order Line Related Items form enables you to review, create, and modify the related items for a customer order line item.OM revamp project - This table has been moved from the order-mgt-review-update-order-line-related-item.dita topic as we're deprecating that topic and removing it from the SOM bundle.The Price Adjustments tab on the order line item details enables you to review and modify manual price adjustments applied to an order line item.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Customer and service order line items forms

The Order Line Items form enables you to select, review, and modify the captured customer or service order line items.

**Parent Topic:**[Order Management reference](order-mgt-reference.md)

## Order Line items form - Details fields

The order line items form line item details section enables you to review and modify general details for a customer or service order line item.

<table id="table-order-li-line-item-detail"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-assigned number of the order line item with a prefix ORDL.

</td></tr><tr><td>

Order

</td><td>

Unique system-assigned number for the customer order. Both customer orders and service orders have an assigned ID with a prefix of ORD.

</td></tr><tr><td>

Product specification

</td><td>

Product specification that is associated with the order line item.

 This field is displayed if the Order type is Product.

</td></tr><tr><td>

Service specification

</td><td>

Service specification that is associated with the order line item. This field is displayed if the Order type is Service.

</td></tr><tr><td>

Product model

</td><td>

Product offering purchased by the customer.

</td></tr><tr><td>

Channel partner

</td><td>

The name of the organization selling a product or service.

</td></tr><tr><td>

State

</td><td>

Indicator of the current processing state for this customer order line item. Unless indicated, the service order manager manually assigns the appropriate state to the service order line item, depending on where it resides in your processing and fulfillment cycle. To view a listing of the state selections, select the down arrow icon ![](../image/field-selection-list.png). **Note:** To view a comprehensive listing of the customer order line item states with detailed descriptions, see [Order line item form states](order-mgt-state-values.md#section-cust-order-line-state).

For service order line item states, see [Service order states](service-order-mgt-state-values.md).

</td></tr><tr><td>

Priority

</td><td>

The priority of completing the order. Options include:

-   1 - Critical
-   2- High
-   3 - Moderate
-   4 - Low

</td></tr><tr><td>

PONR

</td><td>

Option that indicates if this order line item is past the Point of No Return.

-   If selected, it indicates that you can't revise the order line item or request a cancellation for it while the fulfillment process is in progress.
    -   You can't select **Revise Order** or **Cancel Order** to attempt to change the order line item or to request a cancellation for it.
    -   If any of the order line items are designated as PONR, the parent order is also designated as PONR. If the parent order is designated as PONR, the associated line items are also designated as PONR. If any of the line items on an order reaches PONR, you can't revise the other line items on the same order.
-   If cleared, you can still revise the order line item or request a cancellation for it.

The value for this option is a system-assigned flag that you can't manually update.

</td></tr><tr><td>

Order line action

</td><td>

Type of action that is taking place in the order line item. Options include:

-   Add
-   Change
-   Disconnect
-   Suspend
-   Resume
-   No change

 For more information, see [Action types for customer and service orders](../concept/order-mgt-customer-order-types.md).

</td></tr><tr><td>

Action reason

</td><td>

Optional description briefly describing the reason for selecting a specific order line action.

</td></tr><tr><td>

Account

</td><td>

Name of the customer account.

</td></tr><tr><td>

Primary contact

</td><td>

Name of the primary contact person for the account.

</td></tr><tr><td>

Order type

</td><td>

Category that indicates the type of order line item.

-   **Product**

Product order: Customer is ordering a product.

-   **Service**

Service order: Request for the servicing of a product or installation of a service.


**Note:** Like a captured service order, customer orders have an ID with a prefix of **ORD\(nnn\)**. The **Order Category** field enables you to identify the type of order.

</td></tr><tr><td>

Service location

</td><td>

The location or site at which a product needs to be delivered, provisioned, or serviced.

</td></tr><tr><td>

Parent line item

</td><td>

Primary or top-level item in a hierarchical structure of related line items. It represents the main product or service being ordered, while associated child line items represent components, add-ons, or dependent services linked to that parent.

</td></tr><tr><td>

Ordered quantity

</td><td>

Line item order quantity.

</td></tr><tr><td>

Version

</td><td>

Current version of the customer order line item. Indicates the number of times that you revised the customer order line item during the fulfillment process. A new order line item without any revisions has a version of 1 \(one\) and automatically increments for each inflight revision.

</td></tr><tr><td>

Revision operation

</td><td>

Indicates the type of revision operation, if any, that is taking place in the current version of the customer order line item:

-   **None**

No update or cancellation is taking place for the customer order line item. This setting is the default for new customer orders.

-   **Update**

A Characteristic, Contact, or Price inflight revision has been submitted for the customer order line item.

-   **Cancel**

The customer order line item is canceled or in the process of being canceled.


</td></tr><tr><td>

Sales agreement line

</td><td>

If you're using the Sales Agreement Management application and one or more sales agreement were created by an agent, this field shows the system-generated number for the corresponding sales agreement line.

</td></tr><tr><td>

Existing contract

</td><td>

Reference to a previously established customer contract when creating or modifying an order. Existing contracts helps maintain a connection between the current order and the original contract, enabling accurate tracking of changes, renewals, or upsells. It facilitates scenarios where pricing or quantity changes are made to existing contract lines. The system can split line items based on effective start dates and apply delta pricing logic accordingly.

</td></tr><tr><td>

Contract Line type

</td><td>

Indicates the action taken on the contract line, determined by the action type of order line. For instance, 'New' for add orders and 'Amend' for change orders. The available options are:-   No change
-   New
-   Upsell
-   Amend
-   Cancel
-   Renew

</td></tr><tr><td>

Short Description

</td><td>

Short description of the purchased product offering.

</td></tr></tbody>
</table>## Order line items form - date fields

The Order Line Items form - dates section enables you to review and modify crucial date details for a customer order line item.

|Field|Description|
|-----|-----------|
|Planned start date|Planned start date and time for the order line item. It reflects when the product delivery is intended to begin, based on initial scheduling or customer expectations.|
|Planned end date|Planned completion date and time for the order line item. It helps in forecasting delivery timelines and aligning internal resources accordingly.|
|Estimated start date|Projected date and time by which work on the order line item is expected to begin.|
|Estimated end date|Projected date and time by which work on the order line item is expected to conclude.|
|Auto-renew contract|Option to set the automatic renewal of the contract upon expiration.|
|Contract start date|Commencement date of the contract for applying subscription pricing to an order.|
|Contract end date|Date when the contract for a subscription is set to expire.|
|Term \(months\)|Shows the number of months the subscription is valid based on the contract start and end dates.|
|Actual start date|Timestamp when the order line fulfillment or contract execution began. This field is updated once the first fulfillment activity or service activation occurs.|
|Actual end date|Timestamp when the order or contract was completed or terminated. It is used for performance tracking and SLA compliance analysis.|
|Committed due date|Confirmed timestamp by which the which the order line item is expected to be fulfilled or delivered.|
|Effective date|Date on which the order line item becomes active and its terms officially take effect.|
|Expiration date|Date after which the order line item is no longer valid or active.|

## Order line items form - shipping address fields

The Order Line Items form - shipping address details section enables you to review and modify the shipping details for a customer order line item.

|Field|Description|
|-----|-----------|
|Shipping location|Designated site or facility where the order line item should be delivered.|
|Shipping street|Street address of the shipping destination.|
|Shipping city|City where the order line item is to be delivered.|
|Shipping state / Province|State or province of the shipping address.|
|Shipping country|Country where the order line item is being shipped.|
|Shipping zip / Postal code|Postal or zip code for the shipping location.|

## Order line items form - notes fields

The Order Line Items form - notes section enables you to review and modify the additional details for a customer order line item.

<table id="table_rwd_3mb_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional comments

</td><td>

Additional free-form internal comment text for the order line item.

</td></tr><tr><td>

Work notes

</td><td>

Free-form internal work order text for the order line item.

</td></tr><tr><td>

Comments / Work notes \(Private\)

</td><td>

Free-form comment or private work note text:

-   Select the comments icon ![](../image/comments-compose.png) to enter the comment text for the order line item so that everyone, including the customer, can see. Enter the comment text, and then select **Post Comments**.
-   Select the work notes \(private\) icon ![](../image/work-notes-private-compose.png) to enter the work note text for internal purposes only so that the customer can't see it. Enter the work note text, and then select **Post Work notes \(Private\)**.

</td></tr><tr><td>

Activity

</td><td>

Listing of the processing activities, and changes in field values, that have taken place for the order and order line item. This activity includes the messages that indicate the approval of the order for processing and fulfillment. To expand, collapse, or filter by activity stream, do one of the following actions:

-   Select the activity stream filter icon ![](../image/activity-stream-filter.png) to filter by post types, field changes, or flagged items.
-   Select the search icon ![](../image/field-search.png) to search the required information in the activity stream.
-   Select the sort descending icon ![](../../../reuse/icons/product-icons/sort-descending-outline-24.svg) to sort the activity from oldest to newest or select the sort ascending icon ![](../../../reuse/icons/product-icons/sort-ascending-fill-24.svg) for the opposite action.

</td></tr><tr><td>

Attachments

</td><td>

File attachments for the order line item. Select **Select file** to add the file as an attachment. Alternatively, drag a file from your system and drop it into the Attachments pane.

</td></tr></tbody>
</table>## Order line related items fields

The Order Line Related Items form enables you to review, create, and modify the related items for a customer order line item.

|Field|Description|
|-----|-----------|
|Number|Order line related item number.|
|Order line item|Order line item number.|
|Related order line item|Target order line item that the selected order line item is associated with.|
|Specification|Specification name of the related product inventory.|
|Related product inventory|Active product inventory that the selected order line related item is associated with and has a 'Requires' relationship.|

## Price adjustment fields

The Price Adjustments tab on the order line item details enables you to review and modify manual price adjustments applied to an order line item.

<table id="table_d1l_hnq_dfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

ID of the price adjustment record.

</td></tr><tr><td>

Name

</td><td>

Name specified while creating the price adjustment.

</td></tr><tr><td>

Sequence

</td><td>

The number of the pricing plan step used to generate the adjustment. It helps the agent identify the order of operations for the pricing adjustments.

</td></tr><tr><td>

Adjustment source

</td><td>

Origin of the price adjustment.-   Auto: Adjustment applied automatically by pricing plan, and can be defined using standard adjustment matrices or via extension points, such as, PricingAdjustmentExtensionPoint.
-   Manual: Manual adjustment made by agent.

</td></tr><tr><td>

Adjustment type

</td><td>

-   Markdown %
-   Markdown amount
-   Markup %
-   Markup amount
-   Price override

</td></tr><tr><td>

Price point

</td><td>

Setup by the admin in the Pricing Plan for the adjustment step. This could be the List Price or Net Price.

</td></tr><tr><td>

Adjustment value

</td><td>

Percentage or absolute amount of adjustment that is applied to the price.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of items in the order line.

</td></tr><tr><td>

Amount

</td><td>

Price adjustment amount.

</td></tr><tr><td>

Total amount

</td><td>

Quantity multiplied by the amount.

</td></tr><tr><td>

Unit running price

</td><td>

Price calculated with the adjustment amount from the specific pricing plan step.

</td></tr></tbody>
</table>