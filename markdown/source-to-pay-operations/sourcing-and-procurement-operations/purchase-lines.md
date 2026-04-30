---
title: Purchase lines
description: Purchase lines provide information of the individual lines under a purchase requisition or a sourcing request for the referenced supplier.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase lines

Purchase lines provide information of the individual lines under a purchase requisition or a sourcing request for the referenced supplier.

A procurement specialist or procurement administrator can manually create a purchase line, in Pending Review state. Populate the following fields on the purchase line:

-   Legal entity and cost center, based on the specified business owner
-   General ledger account fields, based on the ledger assignment rules
-   Starting unit cost and Negotiated unit cost, based on the supplier product's underlying contractual price
-   Unit, based on the underlying product model of the supplier product

If an ineligible supplier product is selected based on existing shopping controls and the “supplier delivers to” criteria, an error is displayed to the shopper when trying to save the purchase line.

A purchase line can also be created from the intake process. It captures the employee request details for the item that needs to be sourced or purchased.

If sourcing is required for the selected supplier product, a sourcing request is created on saving the purchase line. Updating the status of the sourcing request to Closed Canceled or Closed No Decision corresponds to an update in the status of the associated purchase lines. Credit purchases aren’t enabled in this scenario. The grouping logic determines if the line can be automatically merged with an existing purchase requisition.

The key fields of a purchase line are as follows:

<table id="table_ex2_bps_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the purchase line.

</td></tr><tr><td>

Supplier

</td><td>

Supplier for which the shopper places the order.For a non-catalog intake, if the shopper provides a supplier name for which a supplier record doesn’t exist, a new supplier record is manually created with some of these details:

-   Legal name, according to the name provided by the shopper.
-   Onboarding status of the supplier. An onboarding playbook is triggered for new suppliers as part of Supplier Lifecycle Operations, to guide the registration process for the new supplier contact.
-   Relationship status of the supplier
-   Preferred status of the supplier

The contact details provided by the shopper for the supplier is also displayed as a record in the **Vendor Contacts** related list. This record is created with the help of the vendor contact creation API from Supplier Lifecycle Operations. For more information, see [Create New Supplier Case form](../../supplier-lifecycle-operations/reference/new-supplier-case.md).

</td></tr><tr><td>

Product category

</td><td>

Product category that is sourced through this purchase line.

</td></tr><tr><td>

Supplier product

</td><td>

Supplier product for which the purchase line is created.This field isn’t displayed if the product type is handling fees.

</td></tr><tr><td>

Product name

</td><td>

Name of the supplier product. For a non-catalog purchase, the information is taken from the **Describe the product** or **Describe the service** fields.

This field isn’t displayed if the product type is handling fees.

</td></tr><tr><td>

Product example

</td><td>

Reference URL that the shopper provides. For a non-catalog purchase, this information is obtained from the **Do you have an example of what you're looking for?** field on ShoppingHub.

This field isn’t displayed if the product type is handling fees.

</td></tr><tr><td>

Supplier contacted?

</td><td>

Indicates if the shopper has already contacted the supplier.For a non-catalog purchase, this field is set to true if the shopper selects **I've contacted them already**.

This field isn’t displayed if the product type is handling fees.

</td></tr><tr><td>

Supplier contact

</td><td>

Name of the supplier contact for this supplier.

</td></tr><tr><td>

Supplier contact email

</td><td>

Registered email ID for this supplier contact.

</td></tr><tr><td>

Non-catalog purchase?

</td><td>

Indicates if a non-catalog intake workflow is initiated. The value is true when a shopper uses the **Don't see what you need?** option on ShoppingHub.

This field isn’t displayed if the product type is handling fees.

</td></tr><tr><td>

State

</td><td>

Current status of the purchase line.**Note:** This is a read-only field.

</td></tr><tr><td>

Purchase

</td><td>

Parent purchase associated with this purchase line.

</td></tr><tr><td>

Sourcing request

</td><td>

Sourcing request associated with this purchase line.

</td></tr><tr><td>

Sourcing event

</td><td>

Sourcing event associated with this purchase line.

</td></tr><tr><td>

Negotiation

</td><td>

Negotiation associated with this purchase line.

</td></tr><tr><td>

Purchase requisition

</td><td>

Purchase requisition associated with this purchase line.

</td></tr><tr><td>

Short description

</td><td>

Brief description that is visible to the shopper on ShoppingHub.This field isn’t displayed if the product type is handling fees.

</td></tr><tr><td>

Purchase reason

</td><td>

Reason for the purchase that the shopper provides before checkout.For a non-catalog purchase, this information is obtained from the **Why do you need this?** field on ShoppingHub.

This field isn’t displayed if the product type is handling fees.

</td></tr><tr><td>

Handling fee

</td><td>

Charges added for a specific supplier when a rule is triggered as a result of certain configurable conditions for a purchase requisition being met. For more information on handling fees, see [Handling fees](../concept/handling-fees.md).This field is displayed only if the product type is handling fees.

</td></tr><tr><td>

Specific requirements

</td><td>

Requirements that the shopper specifies. For a non-catalog purchase, this information is given in the **Any specific requirements** field on ShoppingHub.

</td></tr><tr><td class="sub-head" colspan="2">

Purchasing Details

</td></tr><tr><td>

Spend categorization

</td><td>

Indicates whether negotiation with the supplier is addressable or not.

</td></tr><tr><td>

Negotiated by

</td><td>

Indicates who is responsible for negotiation.

</td></tr><tr><td>

Product type

</td><td>

Indicates whether the ordered product type is a good, service, or handling fee.

</td></tr><tr><td>

Goods receipt required

</td><td>

Indicates if a receipt is required in addition to the invoice. This field is visible only if the product type is **Good**.

</td></tr><tr><td>

One-time pricing

</td><td>

Indicates if the pricing created for a service can be reusable in subsequent purchase requests. When created in the context of a sourcing request or negotiation for a service, the default value is **Yes**.This field is visible only if the product type is **Service**.

</td></tr><tr><td>

Expected delivery date

</td><td>

Expected date for the delivery that the shopper requests.**Note:** This date can be in the past, present, or future. For the date to be in the past, the **After the fact** field in the associated purchase requisition table must be set to Yes.

</td></tr><tr><td>

Acknowledgment type

</td><td>

Indicates if receipt of confirmation is necessary and the type of receipt. The available options are **Milestones**, **Service Acknowledgment**, and **Two Way Match**.This field is displayed as **Invoice** if the product type is handling fees.

**Note:** If you’re an existing customer continuing with the Source-to-Pay Common Architecture \(sn\_shop\) plugin, and skipping the Shopping Hub \(sn\_spend\_uib\) plugin, service acknowledgment is replaced with invoice acknowledgment for you.

</td></tr><tr><td>

Milestone payout type

</td><td>

Indicates the type of milestone payout. The options available are **Amount** and **Percentage**.This field is visible only if the acknowledgment type is set to **Milestones**.

</td></tr><tr><td>

Start date

</td><td>

Expected start date of the service that the shopper provides.**Note:** This date can be in the past, present, or future. For the date to be in the past, the **After the fact** field in the associated purchase requisition table must be set to Yes.

</td></tr><tr><td>

End date

</td><td>

Expected date to end providing the service to the shopper.**End date** is calculated as: **Start date**+\[**Term length**\***Term value**\].

**Note:** This date can be in the past, present, or future. For the date to be in the past, the **After the fact** field in the associated purchase requisition table must be set to Yes.

</td></tr><tr><td>

Term length

</td><td>

Duration of the term. When the shopper selects a time frame, the order is considered a blanket type order.

</td></tr><tr><td>

Term value

</td><td>

Type of the term. The options are **Days**, **Weeks**, **Months**, and **Years**.

</td></tr><tr><td>

Maximum budget

</td><td>

Maximum budget that the shopper provides for this purchase.

</td></tr><tr><td>

Purchased quantity

</td><td>

Quantity of the product that the shopper wants to purchase.

</td></tr><tr><td>

Estimated tax

</td><td>

Tax estimate for the product based on the price and delivery location.

</td></tr><tr><td>

Estimated shipping

</td><td>

Shipping cost estimate for the product based on the delivery location.

</td></tr><tr><td>

Total line amount

</td><td>

Total price of the purchased goods and services, including estimated tax and shipping.

</td></tr><tr><td>

Net amount

</td><td>

Amount included as a cost allocation on the purchase order. This doesn’t include any estimates.

</td></tr><tr><td>

Total individual units

</td><td>

Number of fixed assets that are created depends on this value.

</td></tr><tr><td>

Individual unit cost

</td><td>

Cost of the individual unit.

</td></tr><tr><td class="sub-head" colspan="2">

Supplier Bid Details

</td></tr><tr><td>

Supplier's lead time \(days\)

</td><td>

Number of days that the supplier takes to deliver the goods or provide the service. Based on this, the delivery date for goods and the start and end dates for services vary.

</td></tr><tr><td>

Unit

</td><td>

Unit in which the product is provided by the supplier.

</td></tr><tr><td>

Supplier's quantity

</td><td>

Quantity that the supplier can provide.

</td></tr><tr><td>

Starting unit cost

</td><td>

Cost per unit of the product prior to negotiation.

</td></tr><tr><td>

Negotiated unit cost

</td><td>

Cost per unit of the product after negotiation.

</td></tr><tr><td>

Total bid amount

</td><td>

Supplier's quantity multiplied by negotiated unit cost. It reflects the total bid amount from that particular supplier for that purchase line.

</td></tr><tr><td>

Negotiated savings

</td><td>

Total savings through negotiation. This is calculated as: \(Starting unit cost - Negotiated unit cost\) x Supplier's quantity

</td></tr><tr><td>

Supplier notes

</td><td>

Additional notes about the supplier, if any.

</td></tr><tr><td class="sub-head" colspan="2">

Delivery Details

</td></tr><tr><td colspan="2">

Fields in the Delivery Details section map to the information from delivery location details that the shopper provides. Shipping method is displayed as a read-only field here. However, this section isn’t displayed if the product type is handling fees.

</td></tr><tr><td class="sub-head" colspan="2">

Accounting Details

</td></tr><tr><td>

Product category

</td><td>

Category to which the supplier product belongs.

</td></tr><tr><td>

Capex account

</td><td>

Ledger account to post the capital expenses of this product after the purchase completion.

</td></tr><tr><td>

Expense account

</td><td>

Ledger account to post the operational expenses of this product after the purchase completion.

</td></tr><tr><td>

Payment schedule

</td><td>

Indicates the schedule of payments to the supplier.

</td></tr><tr><td>

Pre-payments required

</td><td>

Indicates if pre-payments can be credited to the supplier against this purchase.

</td></tr><tr><td>

Legal entity

</td><td>

Internal legal entity that incurs the cost of this purchase.

</td></tr><tr><td>

Cost center

</td><td>

Cost center that incurs the cost of this transaction.

</td></tr></tbody>
</table>The capex account, expense account, and pre-payment details are populated from [ledger assignment rules](../concept/ledger-assignment-rules.md).

The following are the related lists of a purchase line:

<table id="table_skh_hvs_flb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cases

</td><td>

Displays all the cases associated with this purchase line.

</td></tr><tr><td>

Purchasing Tasks

</td><td>

Provides information of tasks such as obtaining more information from the requester, or awarding a supplier after quotes are received.For details, see [Purchasing tasks and procurement cases](purchasing-tasks.md).

</td></tr><tr><td>

Purchasing SLAs

</td><td>

Provides SLA information for tasks and approvals. The underlying SLA definitions are defined through purchasing SLA definitions, which is an administration module.

</td></tr><tr><td>

Pricing

</td><td>

Stores the relationship between supplier product, contracts, and price of a product.For more details, see [Pricing](pricing.md).

</td></tr><tr><td>

Milestones

</td><td>

Provides information of all the milestones for this purchase. This related list is visible only if the acknowledgment type is set to **Milestones**.

For details, see [Milestones](milestones.md).

</td></tr><tr><td>

Cost Allocations

</td><td>

Provides the information on cost allocation type and the cost center for this purchase line.For details, see [Cost allocations](cost-allocations.md).

</td></tr><tr><td>

Pre-payments

</td><td>

Provides information of the pre-payment details such as the amount and the payment date for this purchase.This related list is visible only if the **Pre-payments required** field is checked.

For details, see [Pre-payments](pre-payments.md).

</td></tr><tr><td>

Contract Requests

</td><td>

Displays all the associated contract requests against this purchase line.**Note:** This field is displayed only if you have the Source-to-Pay Operations with Contract Management Pro plugin \(sn\_spend\_clm\) installed.

</td></tr></tbody>
</table>-   **[Milestones](milestones.md)**  
Milestones represent an acknowledgment that a certain deliverable is achieved for a service. You can create a milestone against the purchase line and purchase order line for a service product type, when the acknowledgment type is set to **Milestones**.
-   **[Cost allocations](cost-allocations.md)**  
Cost allocation defines how to allocate the payment for a particular purchase line. Costs can be allocated towards a cost center, employee credit, or payroll payments.
-   **[Pre-payments](pre-payments.md)**  
A prepayment is the amount paid for services before their receipt or invoiced due date. When an invoice is issued for a pre-payment, it is against the pre-paid account. During the defined pre-paid period, the amount is amortized accordingly against the capex or expense account.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

**Related topics**  


[Purchase revision flows](../concept/purchase-revision-flows.md)

