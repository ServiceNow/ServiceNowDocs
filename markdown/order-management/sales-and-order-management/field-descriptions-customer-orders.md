---
title: Customer and Service order details forms
description: The Order details forms enable you to select, review, and modify captured customer or service orders.The Orders details page - customer order section enables you to review and modify the general details for a product or service order.The Orders details page - pricing section enables you to review and modify the pricing details for a customer or service order.The Orders details page - totals section enables you to review the final total pricing details for a customer or service order.The Orders details page - totals section enables you to review the final total pricing details for a customer or service order.The Orders details page - address section enables you to review and modify the billing and shipping details for a customer or service order.The Orders details page - notes section enables you to review and modify the additional details for a customer or service order.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Customer and Service order details forms

The Order details forms enable you to select, review, and modify captured customer or service orders.

**Parent Topic:**[Order Management reference](order-mgt-reference.md)

## Order details page - Customer Order fields

The Orders details page - customer order section enables you to review and modify the general details for a product or service order.

<table id="table_as2_qdv_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-assigned customer order number.

**Note:** Both customer orders and service orders have an assigned ID with a prefix of ORD. To learn more about order types, see [Order types in Sales Customer Relationship Management](../concept/som-order-types.md).

</td></tr><tr><td>

Account

</td><td>

Name of the customer account.

</td></tr><tr><td>

Contact

</td><td>

Name of the contact for the order.

</td></tr><tr><td>

Channel partner

</td><td>

The name of the organization selling a product or service.

</td></tr><tr><td>

State

</td><td>

Indicator of the current processing state for the customer order, including all of its associated line items. **Note:** To view a comprehensive listing of customer order states with detailed descriptions, see [Customer Order form states](order-mgt-state-values.md#section-cust-order-state) and [Customer order states](order-mgt-state-values.md).

</td></tr><tr><td>

Priority

</td><td>

The priority of completing the order. Options include:-   1 - Critical
-   2- High
-   3 - Moderate
-   4 - Low

</td></tr><tr><td>

External purchase order

</td><td>

A unique identifier or reference number associated with a purchase order issued to a third-party vendor outside the organization to procure goods or services.

</td></tr><tr><td>

Order date

</td><td>

Date that you received the customer order.

</td></tr><tr><td>

Order type

</td><td>

Category that indicates the type of order.

-   **Product**

Product order: Customer is ordering a product.

-   **Service**

Service order: Request for the servicing of a product or installation of a service.


**Note:** Like a captured service order, customer orders have an ID with a prefix of **ORD\(nnn\)**. The **Order Category** field enables you to easily identify the type of order.

</td></tr><tr><td>

Fulfillment type

</td><td>

Type of fulfillment action for the customer order.

-   **Deliver**

Deliver ordered items to the customer when you fulfill the order.

-   **Qualify**

Check the feasibility of delivering the products and services requested on the customer order. Without actually activating or delivering the products or services for the order, it usually processes with a different set of tasks. If all preceding tasks are complete, processing for the associated product, service, or resource order tasks can start.


</td></tr><tr><td>

Version

</td><td>

Current version of the customer order. Indicates the number of times that you revised the customer order during the fulfillment process. A customer order for a product or service can go through multiple revisions during its fulfillment cycle. A new order without any revisions has a version of one, and automatically increments for each inflight revision.

</td></tr><tr><td>

Revision Operation

</td><td>

Type of revision operation, if any, that is taking place in the current version of the customer order:

-   **None**

No update or cancellation is taking place for the customer order. This setting is the default for new customer orders.

-   **Update**

A Characteristic, Contact, or Price inflight revision has been submitted for the customer order.

-   **Cancel**

A customer order is canceled or in the process of being canceled.


</td></tr><tr><td>

Sales agreement

</td><td>

If you're using the Sales Agreement Management application and one or more sales agreement were created by an agent, this field shows the system-generated number for the sales agreement linked to this account. The oldest active agreement is auto-populated. You can manually select any valid agreement from the list.

</td></tr><tr><td>

Existing contract

</td><td>

Reference to a previously established customer contract when creating or modifying an order. Existing contracts helps maintain a connection between the current order and the original contract, enabling accurate tracking of changes, renewals, or upsells. It facilitates scenarios where pricing or quantity changes are made to existing contract lines. The system can split line items based on effective start dates and apply delta pricing logic accordingly.

</td></tr><tr><td>

PONR

</td><td>

Option that indicates if this order is past the Point of No Return.

-   If selected, it indicates that you can't revise the order or request a cancellation for it while the fulfillment process is in progress.
    -   You can't select **Revise Order** or **Cancel Order** to attempt to change the order line item or to request a cancellation for it.
    -   If any of the order line items are designated as PONR, the parent order is also designated as PONR. If the parent order is designated as PONR, the associated line items are also designated as PONR. If any of the line items on an order reaches PONR, you can't revise the other line items on the same order.
-   If cleared, you can still revise the order or request a cancellation for it.

The value for this option is a system-assigned flag that you can't manually update.

</td></tr></tbody>
</table>## Order details page - Pricing fields

The Orders details page - pricing section enables you to review and modify the pricing details for a customer or service order.

<table id="table_dvy_g4b_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order currency

</td><td>

Currency used to place the order. For example, USD for US dollars.

</td></tr><tr><td>

Price list

</td><td>

The price list used for applying prices to the items in your order.

</td></tr><tr><td>

Renewal adjustment basis

</td><td>

Pricing method applied during the renewal of a service contract. It enables agents to specify whether the renewal price should be based on the current market rate or the previously contracted rate. Options include:-   List price: Renews the contract at the current market price of the product or service at the time of renewal.
-   Contracted price: Renews the contract using the original contract price, with optional adjustments

</td></tr><tr><td>

Renewal adjustment type

</td><td>

Method used to adjust the renewal price of a service contract when the value of the Renewal adjustment basis field is set to Contracted price. Options include:-   Markup %: Increases the renewal price by a specified percentage above the contracted price.
-   Markdown %: Decreases the renewal price by a specified percentage below the contracted price.

The field is disabled if the value of the Renewal adjustment basis field is set to List price.

</td></tr><tr><td>

Renewal adjustment value

</td><td>

The actual adjustment value. For example, 10%. If the contracted price is $100 and the adjustment type is Markup % with a value of 10, the renewal price will be $110.

 The field is disabled if the value of the Renewal adjustment basis field is set to List price.

</td></tr></tbody>
</table>## Order details page - Totals fields

The Orders details page - totals section enables you to review the final total pricing details for a customer or service order.

|Field|Description|
|-----|-----------|
|Total one time price|Aggregate cost of all non-recurring charges associated with an order line item. These are typically setup fees, installation charges, or product costs that are billed once rather than on a recurring basis.|
|Total monthly price|The sum of all monthly recurring charges associated with the order.|
|Total annual price|The sum of all annual recurring charges associated with the order.|
|Total amount|Aggregate cost of all charges, both, one-time and recurring, associated with the entire order. It is a calculated field that reflects the final payable amount after applying quantity, pricing, and adjustments.|
|Total net new amount|The total value of newly added products or services in a customer order that are not part of a renewal or amendment. It helps quantify the net new revenue generated from fresh purchases.|

## Order details page - Dates fields

The Orders details page - totals section enables you to review the final total pricing details for a customer or service order.

<table id="table_xbt_fr4_1hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expected start date

</td><td>

Planned start date for the order or contract. It reflects when the service or product delivery is intended to begin, based on initial scheduling or customer expectations.

</td></tr><tr><td>

Expected end date

</td><td>

Planned completion date for the order or contract. It helps in forecasting delivery timelines and aligning internal resources accordingly.

</td></tr><tr><td>

Actual start date

</td><td>

Real date when the order fulfillment or contract execution began. This field is updated once the first fulfillment activity or service activation occurs.

</td></tr><tr><td>

Actual end date

</td><td>

Actual date when the order or contract was completed or terminated. It is used for performance tracking and SLA compliance analysis.

</td></tr><tr><td>

Payment terms

</td><td>

Calendar days by which the buyer must pay the full invoice amount from the invoice date. The available options are:-   None: No payment terms apply.
-   Net 30
-   Net 45
-   Net 60
-   Net 90
-   Due Upon Receipt: Payment is expected immediately once the invoice is received by the buyer.

</td></tr><tr><td>

Auto-renew contract

</td><td>

Option to set the automatic renewal of the contract upon expiration.

</td></tr><tr><td>

Contract start date

</td><td>

Commencement date of the contract for applying subscription pricing to an order.

</td></tr><tr><td>

Contract end date

</td><td>

Date when the contract for a subscription is set to expire.

</td></tr><tr><td>

Term \(months\)

</td><td>

Shows the number of months the subscription is valid based on the contract start and end dates.

</td></tr></tbody>
</table>**Related topics**  


[Add subscription pricing to an order](../task/add-subscription-pricing-to-an-order.md)

## Order details page - Address fields

The Orders details page - address section enables you to review and modify the billing and shipping details for a customer or service order.

|Field|Description|
|-----|-----------|
|Shipping location|Designated site or facility where the order should be delivered.|
|Shipping street|Street address of the shipping destination.|
|Shipping city|City where the order is to be delivered.|
|Shipping state / Province|State or province of the shipping address.|
|Shipping country|Country where the order is being shipped.|
|Shipping zip / Postal code|Postal or zip code for the shipping location.|
|Billing address same as shipping|Option to auto-populate the billing address fields with shipping details.|
|Billing location|Site or office responsible for receiving and processing the invoice.|
|Billing street|Street address for billing purposes.|
|Billing city|City associated with the billing address.|
|Billing state / Province|State or province of the billing address.|
|Billing country|Country where the invoice is sent.|
|Billing zip / Postal code|Postal or zip code for the billing location.|

## Order details page - Notes fields

The Orders details page - notes section enables you to review and modify the additional details for a customer or service order.

<table id="table_qjg_5pq_krb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Special instructions

</td><td>

Optional, custom notes or directions related to the order. These instructions are typically added during the ordering or checkout process and are intended to provide additional context or handling preferences for fulfillment agents.

</td></tr><tr><td>

Work notes

</td><td>

Free-form comment text for internal users.

</td></tr><tr><td>

Additional comments

</td><td>

Extra free-form internal comment text for the customer order.

</td></tr></tbody>
</table><table id="table_l1z_sz4_1hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Comments

</td><td>

Free-form comment text for the customer order that everyone, including the customer, can see.

</td></tr><tr><td>

Work notes

</td><td>

Free-form comment text for internal users.

</td></tr><tr><td>

Activity

</td><td>

Listing of the processing activities, and changes in field values, that have taken place for the order and order line item. This activity includes the messages that indicate the approval of the order for processing and fulfillment.

</td></tr><tr><td>

Attachments

</td><td>

File attachments for the customer or service order. Select **Select file** to add the file as an attachment.

</td></tr></tbody>
</table>