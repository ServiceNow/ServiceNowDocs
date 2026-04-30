---
title: Sourcing events
description: Sourcing events represent the type of sourcing activity needed to negotiate with each supplier, and track the individual negotiations with each supplier. They help sourcing managers manage multi-supplier and multi-product negotiations.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing events

Sourcing events represent the type of sourcing activity needed to negotiate with each supplier, and track the individual negotiations with each supplier. They help sourcing managers manage multi-supplier and multi-product negotiations.

Instead of individually managing negotiations of similar item requests from various suppliers who provide that item, sourcing managers can create a sourcing event for a negotiation intent or objective to manage multi-supplier and multi-product negotiations. Multiple negotiations and sourcing requests can be mapped to a single sourcing event as child entities.

Through this sourcing event, the sourcing managers can view and effectively manage the progress of the negotiations created for each supplier​. They can also discuss, follow, update, or cancel the event, as required. Further, they can award a single supplier or multiple suppliers, or even reject bids by selecting **Award**, **Award multiple suppliers**, or **Reject bids** respectively. Selecting **Award multiple suppliers** redirects them to the Source-to-Pay Workspace, where they can complete the process. For more information on this, see [Award multiple suppliers from a sourcing event](../task/award-multiple-suppliers-from-a-ne.md).

Sourcing events can be best viewed from the Source-to-Pay Workspace list page.

Here’s a list of key fields of a sourcing event:

<table id="table_h1y_gj5_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the sourcing event.

</td></tr><tr><td>

Assigned to

</td><td>

User who is responsible for the sourcing event.

</td></tr><tr><td>

State

</td><td>

Current state of the sourcing event.**Note:** This is a read-only field.

</td></tr><tr><td>

Supplier responses close

</td><td>

Date by which the suppliers must submit their responses to the sourcing activity.

</td></tr><tr><td>

Short description

</td><td>

Brief of the sourcing event.

</td></tr><tr><td>

Description

</td><td>

Details of the sourcing event.

</td></tr><tr><td class="sub-head" colspan="2">

Summary

</td></tr><tr><td>

Negotiation type

</td><td>

Type of sourcing event or the method used to engage with the supplier. For example, you can initiate a contract renewal or ask for a quote.

</td></tr><tr><td>

Negotiation outcome

</td><td>

Anticipated outcome or end results of the sourcing event. For example, you can negotiate contract terms or standard savings on a purchase.

</td></tr><tr><td>

Expected start

</td><td>

Expected start date of the sourcing event.

</td></tr><tr><td>

Actual start

</td><td>

Actual start date of the sourcing event.

</td></tr><tr><td>

Actual end

</td><td>

Actual end date of the sourcing event.

</td></tr><tr><td>

Duration

</td><td>

Duration of the sourcing event.

</td></tr><tr><td>

Negotiation objectives

</td><td>

Objectives or goals for the sourcing event.

</td></tr><tr><td>

Close notes

</td><td>

Notes on closure of the sourcing event, if any.

</td></tr></tbody>
</table>The following are the related lists of a sourcing event:

<table id="table_ddt_2ct_flb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sourcing Requests

</td><td>

View all the sourcing requests that are mapped to this sourcing event.For details, see [Sourcing request](sourcing-request.md).

</td></tr><tr><td>

Negotiations

</td><td>

View all the negotiations with each supplier that are mapped to this sourcing event.For details, see [Negotiations](negotiations.md).

</td></tr><tr><td>

Purchase Lines

</td><td>

View and track all the purchase line records within the parent purchase for the suppliers referenced on the sourcing event.For details, see [Purchase lines](purchase-lines.md).

</td></tr><tr><td>

Purchasing Tasks

</td><td>

View information on all the purchasing tasks that are related to the sourcing event. For details, see [Purchasing tasks and procurement cases](purchasing-tasks.md).

</td></tr><tr><td>

Cases

</td><td>

View information on all the cases that are related to the negotiation event.

</td></tr><tr><td>

Draft Contracts

</td><td>

View and track all the draft contracts for the suppliers referenced on the sourcing event. For more details, see [Contracts](contracts.md).

</td></tr><tr><td>

Signed Contracts

</td><td>

View and track all the signed contracts for the suppliers referenced on the sourcing event.

</td></tr><tr><td>

Other Legal Documents

</td><td>

View and track all the other legal documents for the suppliers referenced on the sourcing event.

</td></tr><tr><td>

Contract Requests

</td><td>

Displays all the associated contract requests against this sourcing event.**Note:** This field is displayed only if you have the Source-to-Pay Operations with Contract Management Pro plugin \(com.snc.sn\_spend\_clm\) installed.

</td></tr><tr><td>

Purchase SLAs

</td><td>

View all the purchase SLAs associated to purchasing tasks against the sourcing event, along with tasks associated to the underlying purchase requisition lines.

</td></tr><tr><td>

Purchase Requisitions

</td><td>

View information on all the purchase requisitions that are related to the sourcing event.For more details, see [Purchase requisition](purchase-requisition.md).

</td></tr><tr><td>

Draft Emails

</td><td>

Associated email communication that is saved as drafts.

</td></tr><tr><td>

Sent Emails

</td><td>

Associated email communication that has been sent.

</td></tr></tbody>
</table>## Sourcing event workflow

![Sourcing event workflow](../image/ne-workflow.png)

The default states that are available for a sourcing event are listed.

-   Draft
-   Planned
-   Work in Progress
-   Pricing Obtained
-   Awaiting Task Completion
-   Requires Decision
-   Closed Complete
-   Closed No Decision
-   Closed Canceled

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

