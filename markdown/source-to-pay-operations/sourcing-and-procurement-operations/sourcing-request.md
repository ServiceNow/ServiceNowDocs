---
title: Sourcing request
description: A sourcing request is created for when an item that a shopper, employee, or requester needs, must be sourced. This record is created when an active contractual price for the product that the shopper intends to purchase doesn’t exist. This includes items in both the product catalog and off-catalog.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing request

A sourcing request is created for when an item that a shopper, employee, or requester needs, must be sourced. This record is created when an active contractual price for the product that the shopper intends to purchase doesn’t exist. This includes items in both the product catalog and off-catalog.

A purchase line is created, which is then grouped into a sourcing request. Sourcing requests are grouped by product models.

As a procurement specialist or sourcing manager:

-   To view all sourcing requests from the Source-to-Pay Workspace, navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**, and select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\), followed by **All team work** &gt; **Sourcing Requests**.
-   To view all sourcing requests from the Platform, navigate to **Sourcing and Purchasing Automation** &gt; **All Work**, and select **All Sourcing Requests**.
-   To view sourcing requests assigned to you from the Platform, navigate to **Sourcing and Purchasing Automation** &gt; **My Work**, and select **My Sourcing Requests**.

After the shopper places a request for a catalog or non-catalog item from ShoppingHub, the information that the shopper provides is mapped to the fields of a sourcing request as follows:

<table id="table_x3l_cdt_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the sourcing request.

</td></tr><tr><td>

Assigned to

</td><td>

User who is responsible for the purchase. Determined using purchasing assignment rules. For details, see [Create a purchasing assignment rule](../task/create-purchasing-assignment-rule.md).

</td></tr><tr><td>

Business owner

</td><td>

User who owns the sourcing request.

</td></tr><tr><td>

Submitted by

</td><td>

User who has shopped and submitted the purchase.

</td></tr><tr><td>

Status

</td><td>

Status of the sourcing request.**Note:** This is a read-only field.

</td></tr><tr><td>

Purchase

</td><td>

Related purchase, if any.

</td></tr><tr><td>

Sourcing event

</td><td>

Represents the type of sourcing activity needed to negotiate with each supplier, and tracks the individual negotiations with each supplier.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the sourcing request.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Product category

</td><td>

Product category that is sourced through this sourcing request.

</td></tr><tr><td>

Product model

</td><td>

Product model that is sourced through this sourcing request.

</td></tr><tr><td>

Product name

</td><td>

Product that is requested for.

</td></tr><tr><td>

Product type

</td><td>

Indicates if the type of the product is a good or service.

</td></tr><tr><td>

Supplier responses close

</td><td>

Date by which the suppliers must submit their responses to the sourcing activity.

</td></tr><tr><td>

Benchmark price

</td><td>

Price point from which all starting unit costs for all the purchase lines of this sourcing requests are derived.

</td></tr><tr><td>

Request type

</td><td>

Type of request that the shopper, employee, or requester is asking for. The options are request for quote, request for information, request for proposal, and proof of concept.

</td></tr><tr><td>

Sourcing request details

</td><td>

Details of the sourcing request.

</td></tr></tbody>
</table>The following are the related lists of a sourcing request record:

<table id="table_svr_qws_flb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase Lines

</td><td>

Provides information of the individual lines under a sourcing request for the referenced supplier. The number of purchase lines for a sourcing request depends on the number of products or services with the same product model.

For more details, see [Purchase lines](purchase-lines.md).

</td></tr><tr><td>

Purchasing Tasks

</td><td>

Provides information of all purchasing tasks that are related to the sourcing request​. The tasks on the associated negotiation aren’t displayed.For more details, see [Purchasing tasks and procurement cases](purchasing-tasks.md).

</td></tr><tr><td>

Cases

</td><td>

Displays all the cases associated with this sourcing request.

</td></tr><tr><td>

Purchasing SLAs

</td><td>

Displays the SLAs associated to purchasing tasks against the sourcing request, along with tasks associated to the underlying purchase requisition line.

</td></tr><tr><td>

Negotiations

</td><td>

Represents the task of obtaining the pricing of or negotiating the terms for the product or service requested by the shopper.For more details, see [Negotiations](negotiations.md).

</td></tr><tr><td>

Draft Contracts

</td><td>

Displays all the draft contracts associated with this sourcing request.For more details, see [Contracts](contracts.md).

</td></tr><tr><td>

Signed Contracts

</td><td>

Displays all the signed contracts associated with this sourcing request.

</td></tr><tr><td>

Other Legal Documents

</td><td>

Displays all the other legal documents associated with this sourcing request.

</td></tr><tr><td>

Contract Requests

</td><td>

Displays all the associated contract requests against this sourcing request.**Note:** This field is displayed only if you have the Source-to-Pay Operations with Contract Management Pro plugin \(com.snc.sn\_spend\_clm\) installed.

</td></tr><tr><td>

Approval Plans

</td><td>

Displays all the approval plans created against this sourcing request.

</td></tr><tr><td>

Draft Emails

</td><td>

Associated email communication that is saved as drafts.

</td></tr><tr><td>

Sent Emails

</td><td>

Associated email communication that has been sent.

</td></tr></tbody>
</table>## Sourcing and negotiation workflow

![Sourcing and negotiation workflow](../image/sourcing-workflow.png)

After a sourcing request is created, the procurement specialist can create a purchasing task of the subtype **Ask a question** if more details are needed from the shopper.

The procurement specialist can decide if a negotiation for this purchase can be created or not. If time doesn’t permit for a negotiation, the supplier can be contacted directly for pricing details. After the suppliers respond with their quotes, a purchasing task is systematically created requesting the shopper to select a supplier to award. This is a sourcing task of the subtype **Select a supplier**. For an awarded supplier, the Awarded column value of a purchase line is automatically set to **Yes**, and this creates an associated purchase requisition.

A shopper can select **Cancel** to update the status of the sourcing request and its associated purchase lines to Closed Canceled.

## Sourcing request state flows

Let's consider a simple scenario where qualification is needed. If a price is entered on a purchase line \(PRL\), the PRL indicates that the price has been added or updated, and moves to the Pricing Obtained state, where it remains in that state. All the other PRLs without price and the sourcing request \(SR\) continue to remain in the Qualification Needed state. Once qualified, the SR and other PRLs that are in the Qualification Needed state move to the Qualified state, while the PRL that had price remain in the Pricing Obtained state.

Manually creating a new PRL re-triggers the qualification flow. If pricing has been added to this PRL, the PRL remains in the Pricing Obtained state while qualification work is being done. The SR also remains in the Qualification Needed state, as needed.

When sourcing events \(NEs\) and negotiations \(NEGs\) are considered in the sourcing flow, consider the following scenarios:

-   Qualification is needed, where NE is in the Planned state, and NEG, SR, and PRL are all in the Qualification Needed state:

    If a price is entered on a PRL, the PRL indicates that the price has been added or updated, and moves to the Pricing Obtained state, where it remains in that state. All the other PRLs without price and the SR continue to remain in the Qualification Needed state. Once qualified, the SR and other PRLs that are in the Qualification Needed state move to the Qualified state, while the PRL that had price remain in the Pricing Obtained state.

-   NEG is in progress, where NE is in WIP, and NEG, SR, and PRL are all in the Negotiation in Progress state:

    If a price is entered on a PRL when NEG is in progress, the PRL indicates that the price has been added or updated, and moves to the Pricing Obtained state, where it remains in that state. All the other PRLs without price and the NEG and SR remain in the Negotiation in Progress state, while the NE remains in WIP.

-   New SRs or suppliers are added after **Start negotiating** is selected on the NE, where NE is in WIP, and NEG, SR, and PRL are all in the Negotiation in Progress state:

    This triggers qualification cases to be evaluated on the affected PRLs and move the NEG to Qualification Needed. If qualification isn’t needed, both the NEGs and the newly created PRLs remain in the Negotiation in Progress state.

    If qualification is needed, NEs remain in WIP even when new SRs or existing suppliers are added. Once qualification cases are complete, Individual NEGs automatically move from Qualified to Negotiation in Progress, without the need to re-select **Start negotiating** on the NE. The newly evaluated PRLs also move to Negotiation in Progress.

    However, at any point, if a price is entered on any of the newly created PRLs, the PRL indicates that the price has been added or updated, and moves to the Pricing Obtained state, where it remains in that state.


The default states that are available for a sourcing request are listed.

-   Pending Approval
-   Pending Review
-   Information Needed
-   Qualification Needed
-   Qualified
-   Pending Negotiation
-   Negotiation in Progress
-   Pending Resubmission
-   Awaiting Supplier Response
-   Awaiting Task Completion
-   Requires Decision
-   Closed Complete
-   Closed No Decision
-   Closed Canceled
-   Closed Rejected

For more information on NEGs and NEs, see [Negotiations](negotiations.md) and [Sourcing events](negotiation-events.md) respectively.

For information on how a supplier tiering assessment task influences SR states, see [Sourcing and Procurement Operations integration with Third-party Risk Management](../concept/better-together-with-vrm.md).

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

