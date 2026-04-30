---
title: Negotiations
description: A negotiation represents individual supplier negotiations and tracks the items and activities according to supplier. These activities involve obtaining the price for the products or services requested by the shopper, or negotiating the terms.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Negotiations

A negotiation represents individual supplier negotiations and tracks the items and activities according to supplier. These activities involve obtaining the price for the products or services requested by the shopper, or negotiating the terms.

The type and outcome of a negotiation record can be used for reporting purposes.

Here’s a list of key fields of a negotiation:

<table id="table_h1y_gj5_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the negotiation.

</td></tr><tr><td>

Assigned to

</td><td>

User who is responsible for the negotiation.

</td></tr><tr><td>

State

</td><td>

Current status of the negotiation.**Note:** This is a read-only field.

</td></tr><tr><td>

Due date

</td><td>

Date when this negotiation is scheduled to be completed.

</td></tr><tr><td>

Short description

</td><td>

Brief of the negotiation.

</td></tr><tr><td class="sub-head" colspan="2">

Summary

</td></tr><tr><td>

Negotiation event

</td><td>

Negotiation event associated with this negotiation.

</td></tr><tr><td>

Supplier

</td><td>

Supplier with whom you are negotiating.

</td></tr><tr><td>

Negotiation type

</td><td>

Type of negotiation with the supplier. For example, you can initiate a contract renewal or ask for a quote.

</td></tr><tr><td>

Negotiation outcome

</td><td>

Result of the negotiation. For example, you can negotiate contract terms or savings on a purchase.

</td></tr><tr><td>

Expected start

</td><td>

Expected start date of the negotiation.

</td></tr><tr><td>

Actual start

</td><td>

Actual start date of the negotiation.

</td></tr><tr><td>

Actual end

</td><td>

Actual end date of the negotiation.

</td></tr><tr><td>

Duration

</td><td>

Duration of the negotiation.

</td></tr><tr><td>

Negotiation objectives

</td><td>

Objectives or goals for the negotiation.

</td></tr><tr><td>

Close notes

</td><td>

Notes on closure of the negotiation, if any.

</td></tr></tbody>
</table>The following are the related lists of a negotiation:

<table id="table_ddt_2ct_flb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sourcing Requests

</td><td>

View and track all the sourcing requests associated with the purchase lines in the negotiation​.For details, see [Sourcing request](sourcing-request.md).

</td></tr><tr><td>

Purchase Lines

</td><td>

View and track all the purchase line records within the parent purchase for the supplier referenced on the negotiation.For details, see [Purchase lines](purchase-lines.md).

</td></tr><tr><td>

Purchasing Tasks

</td><td>

View information on all the purchasing tasks that are related to the negotiation. For details, see [Purchasing tasks and procurement cases](purchasing-tasks.md).

</td></tr><tr><td>

Cases

</td><td>

View information on all the cases that are related to the negotiation event.

</td></tr><tr><td>

Draft Contracts

</td><td>

View and track all the draft contracts for the supplier referenced on the negotiation. For more details, see [Contracts](contracts.md).

</td></tr><tr><td>

Signed Contracts

</td><td>

View and track all the signed contracts for the supplier referenced on the negotiation.

</td></tr><tr><td>

Other Legal Documents

</td><td>

View and track all the other legal documents for the supplier referenced on the negotiation.

</td></tr><tr><td>

Contract Requests

</td><td>

Displays all the associated contract requests against this negotiation.**Note:** This field is displayed only if you have the Source-to-Pay Operations with Contract Management Pro plugin \(com.snc.sn\_spend\_clm\) installed.

</td></tr><tr><td>

Purchasing SLAs

</td><td>

View all the purchasing SLAs associated to the purchasing tasks against the negotiation, along with tasks associated to the underlying purchase requisition line.

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

## Negotiation state flows

The status of the purchase line and the sourcing request updates automatically depending on the status of the negotiation. Negotiations are grouped by supplier.

-   When the state of the negotiation is updated to Awaiting Supplier Response, all applicable purchase requisition lines, for the same supplier, of sourcing requests associated to the negotiation are also updated to Awaiting Supplier Response. The purchase requisition lines not belonging to sourcing requests associated to the negotiation aren’t updated.
-   When all applicable purchase requisition lines, for the same supplier, of sourcing requests associated to the negotiation are updated to Pricing Obtained, the state of the negotiation should be Closed Complete. If one purchase requisition line is in Pricing Obtained state, while another is still in Awaiting Supplier Response, the state of the negotiation remains in the Awaiting Supplier Response state.
-   When the state of the negotiation is updated to Negotiation in Progress, all applicable purchase requisition lines, for the same supplier, of sourcing requests associated to the negotiation are updated to Negotiation in Progress. The purchase requisition lines not belonging to sourcing requests associated to the negotiation aren’t updated.
-   When the state of the negotiation is updated to Closed Complete or Closed Canceled, no state updates are affected on the purchase requisition lines.

The default states that are available for a negotiation are listed.

-   Planned
-   Qualification Needed
-   Qualified
-   Negotiation in Progress
-   Awaiting Supplier Response
-   Pricing Obtained
-   Awaiting Task Completion
-   Requires Decision
-   Closed Decided
-   Closed No Decision
-   Closed Rejected
-   Closed Canceled

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

