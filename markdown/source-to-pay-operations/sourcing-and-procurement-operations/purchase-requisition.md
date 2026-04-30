---
title: Purchase requisition
description: A purchase requisition represents a request that is sent internally within an organization to obtain purchased goods or services. It consists of items that need to be ordered, and may need to go through approvals for a purchase order to be created.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase requisition

A purchase requisition represents a request that is sent internally within an organization to obtain purchased goods or services. It consists of items that need to be ordered, and may need to go through approvals for a purchase order to be created.

A purchase requisition is created in either of the following scenarios:

-   When a shopper selects **Request to buy** from a product details page on ShoppingHub.
-   When a supplier is selected after providing quotes in a sourcing request.

Through a purchase requisition, the purchasing department understands details of the items that are requested, the quantity, supplier, cost, and reason for purchase.![Purchase requisition.](../image/create_purchase_requisition.png)

<table id="table_a5j_d3r_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the purchase requisition.

</td></tr><tr><td>

Requisition type

</td><td>

Indicates if this requisition is net new or a revision.The shopper can revise the quantity of the product or delivery location for on order from ShoppingHub or the buyer can submit a revision from the Sourcing and Purchasing Automation module.

To understand how revisions are handled, see [Purchase revisions](purchase-revisions.md).

</td></tr><tr><td>

Assigned to

</td><td>

User who is responsible for the purchase. Determined using purchasing assignment rules.

</td></tr><tr><td>

Primary contact

</td><td>

Person within the procurement team working on the purchase who can be contacted with questions. This field is populated or updated with the same user in the **Assigned to** field on the purchase requisition.

</td></tr><tr><td>

Business owner

</td><td>

User who submitted the purchase request.

</td></tr><tr><td>

Submitted by

</td><td>

User who has shopped and submitted the purchase.

</td></tr><tr><td>

State

</td><td>

Status of the purchase requisition.**Note:** This is a read-only field.

</td></tr><tr><td>

Purchase

</td><td>

Unique ID of the purchase.

</td></tr><tr><td>

Negotiation

</td><td>

Negotiation associated with this purchase requisition.

</td></tr><tr><td>

Purchase order

</td><td>

Purchase order associated with this purchase requisition.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the purchase requisition.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Supplier

</td><td>

Indicates the supplier who provides the product.

</td></tr><tr><td>

Order type

</td><td>

Indicates whether the resulting order is a standard or blanket order.During the checkout of a product or service, if the shopper selects a time frame for the delivery based on date range or term, the order type is considered as **Blanket**.

Otherwise, the order type is considered as **Standard**.

</td></tr><tr><td>

After the fact

</td><td>

Indicates if the purchase requisition is after the fact or not.After a purchase line is created and grouped into a purchase requisition, if the created on date is either within or after x number of days of the expected delivery date or start date, then the entire purchase requisition would be considered as after the fact. For a purchase requisition that has multiple purchase lines, if at least one line is after the fact, the entire purchase requisition is considered after the fact.

</td></tr><tr><td>

Requested delivery

</td><td>

Requested delivery date.**Note:** This can be a date or date range that is in the past, present, or future. For the date to be in the past, the **After the fact** field must be set to Yes.

</td></tr><tr><td>

Shipping method

</td><td>

Details of the carrier, the applicable suppliers, and the valid delivery location countries for those suppliers.For more information on shipping methods and handling fees, see [Handling fees](../concept/handling-fees.md).

</td></tr><tr><td>

Total estimated tax

</td><td>

The estimated sum of all taxes related to purchase lines within a purchase requisition.

</td></tr><tr><td>

Total estimated shipping

</td><td>

Estimated sum of all shipping costs related to purchase lines within a purchase requisition.

</td></tr><tr><td>

Discount percentage

</td><td>

Discount provided if the minimum spend requirement is met.This field isn’t displayed for a blanket order type.

</td></tr><tr><td>

Minimum spend

</td><td>

Minimum amount that must be spent to avail a discount.This field isn’t displayed for a blanket order type.

</td></tr><tr><td>

Total amount

</td><td>

Total cost of purchase requisition calculated as the sum from all purchase lines.

</td></tr><tr><td class="sub-head" colspan="2">

Accounting Details

</td></tr><tr><td>

Payment term

</td><td>

Payment term as agreed with the supplier. This value defaults from the referenced supplier record.

</td></tr><tr><td>

Legal entity

</td><td>

This value defaults from the associated business owner.

</td></tr><tr><td>

Purchasing entity

</td><td>

This value defaults from the associated business owner.

</td></tr><tr><td>

Cost center

</td><td>

This value defaults from the associated business owner.**Note:** This value must be filled on the Business Owner record for it to be populated on the purchase requisition.

</td></tr></tbody>
</table>The following are the related lists of a purchase requisition:

<table id="table_r2v_bmr_flb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase Lines

</td><td>

Provides information of the individual lines under a purchase requisition for the referenced supplier. Handling fees, if applicable, are added as a purchase line for this purchase requisition. For more details, see [Purchase lines](purchase-lines.md).For information on shipping methods and handling fees, see [Handling fees](../concept/handling-fees.md).

</td></tr><tr><td>

Purchasing Tasks

</td><td>

Provides information of all purchasing tasks that must be completed prior to creation of a purchase order​.For more details, see [Purchasing tasks and procurement cases](purchasing-tasks.md).

</td></tr><tr><td>

Purchasing SLAs

</td><td>

Provides SLA information for tasks and approvals. The underlying SLA definitions are defined through purchasing SLA definitions, which is an administration module.

</td></tr><tr><td>

Cases

</td><td>

Displays all the cases associated with this purchase requisition.

</td></tr><tr><td>

Related Contracts

</td><td>

Provides information of all active and draft contracts for the referenced supplier​.

</td></tr><tr><td>

Purchasing Permissions

</td><td>

This related list is conditionally displayed for purchase requisitions whose order type is **Blanket**.Purchasing permissions enable a user to define a list of pre-approved users, groups, departments, or cost centers. Any purchases made by these users against the blanket purchase order don’t require an approval process.

By default, the business owner on the originating purchase requisition of order type **Blanket** is added as a user that can create a standard release against a blanket purchase order.

</td></tr><tr><td>

Related Purchase Requisition

</td><td>

This related list is conditionally displayed for revised requisitions. It shows the relationship between the original and revised purchase requisitions.

</td></tr><tr><td>

Approval Plans

</td><td>

Displays all the approval plans created against this purchase requisition.

</td></tr><tr><td>

Approvals

</td><td>

Displays the list of approvers that must approve the purchase requisition.

</td></tr><tr><td>

Contract Requests

</td><td>

Displays all the associated contract requests against this purchase requisition.**Note:** This field is displayed only if you have the Source-to-Pay Operations with Contract Management Pro plugin \(sn\_spend\_clm\) installed.

</td></tr><tr><td>

Draft Emails

</td><td>

Associated email communication that is saved as drafts.

</td></tr><tr><td>

Sent Emails

</td><td>

Associated email communication that has been sent.

</td></tr></tbody>
</table>The key purchasing properties relevant to a purchase requisition are:

-   sn\_shop.atf.threshold.days
-   sn\_shop.spend.requisition.autoorder
-   sn\_shop.spend.requisition.autoorder.threshold
-   sn\_shop.approval.reassessment.resend

For the list of all purchasing properties, see [Purchasing properties](installed-with-FSC.md#section_fls_xdt_flb). If you have the role of a procurement administrator, you can access the Purchasing Properties module by navigating to **Sourcing and Purchasing Automation** &gt; **Administration**.

The default states that are available for a purchase requisition are listed.

-   Pending Review
-   Pending Approval
-   Awaiting Task Completion
-   Final Review
-   Pending Submission
-   Closed Complete
-   Closed Canceled
-   Closed Rejected
-   Pending Cancellation
-   Pending Revision
-   Pending Supplier Confirmation

-   **[Handling fees](../concept/handling-fees.md)**  
As an administrator, you can configure the conditions of a purchase request, which when met, adds a handling fee to that purchase request. Any field on the Purchase Request table can be used as part of the conditions to determine if a handling fee is to be applied for a purchase.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

