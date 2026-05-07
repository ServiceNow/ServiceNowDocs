---
title: Purchase requisition, purchase order, and sourcing request states
description: Purchase requisitions, purchase orders, and sourcing requests move through a series of states as they progress through the procurement lifecycle. Each state reflects the current stage of processing and determines what actions are available.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-04-14"
reading_time_minutes: 9
keywords: [purchase requisition states, purchase order states, sourcing request states, state transitions, procurement lifecycle, Sourcing and Procurement Operations]
breadcrumb: [Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase requisition, purchase order, and sourcing request states

Purchase requisitions, purchase orders, and sourcing requests move through a series of states as they progress through the procurement lifecycle. Each state reflects the current stage of processing and determines what actions are available.

## How states are determined

The state of a purchase requisition, purchase order, or sourcing request is calculated automatically based on the states of its associated lines. When a line changes state, the system recalculates and updates the parent record's state. You cannot set the state of these records directly.

When procurement cases or purchasing tasks are associated with a record, the state reflects whether those items are still open. For example, a purchase requisition remains in the Awaiting Task Completion state until all order-dependent cases and tasks are closed.

## Purchase requisition states

The following table describes each purchase requisition state, when the state is set, and where the purchase requisition can move from that state.

<table><thead><tr><th>

State

</th><th>

When this state is set

</th><th>

Next state

</th></tr></thead><tbody><tr><td>

Pending Review

</td><td>

Set when the purchase requisition is first created, or when any purchase requisition line requires review. This is the initial state for all purchase requisitions.

</td><td>

-   Pending Approval
-   Awaiting Task Completion
-   Closed Canceled
-   Closed Rejected

</td></tr><tr><td>

Pending Approval

</td><td>

Set when all purchase requisition lines have completed review and are awaiting approval. No lines remain in the Pending Review state.

</td><td>

-   Awaiting Task Completion
-   Final Review
-   Closed Rejected

</td></tr><tr><td>

Awaiting Task Completion

</td><td>

Set when all purchase requisition lines are approved, but one or more order-dependent procurement cases or purchasing tasks associated with the purchase requisition are still open. The state is updated automatically when all blocking cases and tasks are closed.

</td><td>

Final Review \(when all blocking cases and tasks are closed\)

</td></tr><tr><td>

Final Review

</td><td>

Set when all purchase requisition lines are approved and no open procurement cases or purchasing tasks are blocking the purchase requisition. The purchase requisition is ready for submission.

</td><td>

-   Pending Submission \(when buyer submits\)
-   Pending Revision \(if a revision is triggered\)

</td></tr><tr><td>

Pending Submission

</td><td>

Set when the purchase requisition has been approved and submitted, and a purchase order is being created or processed. This is an intermediate state during order creation.

</td><td>

-   Closed Complete \(when the order is fulfilled\)
-   Closed Canceled \(if canceled before ordering\)

</td></tr><tr><td>

Pending Supplier Confirmation

</td><td>

Set when the purchase order has been submitted to the supplier and the system is waiting for an explicit supplier acknowledgment before the order is confirmed.

</td><td>

-   Pending Submission \(if not confirmed\)
-   Closed Complete \(when confirmed and fulfilled\)

</td></tr><tr><td>

Pending Cancellation

</td><td>

Set when a cancellation has been requested for the purchase requisition and one or more lines are awaiting cancellation confirmation.

</td><td>

Closed Canceled \(when cancellation is confirmed\)

</td></tr><tr><td>

Pending Revision

</td><td>

Set when a buyer or procurement specialist triggers a revision of the purchase requisition and one or more lines are in revision. No lines are in a higher-priority state.

</td><td>

Pending Review \(when the revised purchase requisition is resubmitted\)

</td></tr><tr><td>

Closed Complete

</td><td>

Set when all purchase requisition lines have reached a closed complete state, indicating that goods or services have been received and matched.

</td><td>

Not applicable. This is the last state.

</td></tr><tr><td>

Closed Canceled

</td><td>

Set when all purchase requisition lines have been canceled and no lines remain in an active state.

</td><td>

Not applicable. This is the last state.

</td></tr><tr><td>

Closed Rejected

</td><td>

Set when all purchase requisition lines have been rejected. When the primary line is rejected, all associated lines are also set to rejected.

</td><td>

Not applicable. This is the last state.

</td></tr></tbody>
</table>## Purchase order states

The following table describes each purchase order state, when the state is set, and where the purchase order can move from that state. Purchase order states are calculated based on the states of the associated purchase order lines.

<table><thead><tr><th>

State

</th><th>

When this state is set

</th><th>

Next state

</th></tr></thead><tbody><tr><td>

Processing

</td><td>

Set when the purchase order is being generated or processed by an automated integration, such as an ERP system. This is an intermediate state while external processing completes.

</td><td>

Pending Submission \(when processing is complete\)

</td></tr><tr><td>

Pending Revision

</td><td>

Set when the purchase order has been revised through a purchase modification case and is awaiting resubmission to the supplier.

</td><td>

Pending Submission \(when the revision is resubmitted\)

</td></tr><tr><td>

Pending Submission

</td><td>

Set when purchase order lines are ready to be transmitted to the supplier. Entered from Processing when ERP processing completes, or from Pending Revision after a revision is resubmitted.

</td><td>

-   Ordered \(when submission is confirmed\)
-   Pending Supplier Confirmation \(if supplier acknowledgment is required\)

</td></tr><tr><td>

Pending Supplier Confirmation

</td><td>

Set when the purchase order has been submitted to the supplier and the system is waiting for an explicit supplier acknowledgment before the order is treated as confirmed.

</td><td>

Ordered \(when the supplier confirms\)

</td></tr><tr><td>

Ordered

</td><td>

Set when all purchase order lines have been submitted and confirmed by the supplier, or auto-confirmed. No lines are pending, in revision, or partially delivered.

</td><td>

-   Partially Delivered
-   Delivered \(as goods or services are received\)

</td></tr><tr><td>

Partially Delivered

</td><td>

Set when some purchase order lines have been received and others are still in an ordered state, or when at least one line is explicitly partially delivered.

</td><td>

Delivered \(when all lines are received\)

</td></tr><tr><td>

Delivered

</td><td>

Set when all purchase order lines have been received. The purchase order is awaiting invoice processing.

</td><td>

-   Payment Pending \(when an invoice is created\)
-   Closed Released \(if no invoice is required\)

</td></tr><tr><td>

Payment Pending

</td><td>

Set when an invoice has been received and matched to the purchase order, and payment is pending.

</td><td>

Closed Paid \(when the invoice is paid\)

</td></tr><tr><td>

Pending Return

</td><td>

Set when a return has been initiated for one or more purchase order lines.

</td><td>

-   Closed Returned \(when the return is processed\)
-   Ordered \(if the return is reversed\)

</td></tr><tr><td>

Pending Cancellation

</td><td>

Set when a cancellation has been requested for the purchase order but has not yet been confirmed.

</td><td>

-   Closed Canceled \(when cancellation is confirmed\)
-   Ordered \(if the cancellation is reversed\)

</td></tr><tr><td>

Closed Paid

</td><td>

Set when the invoice has been paid and all purchase order lines are in a paid state.

</td><td>

Closed Released \(after final reconciliation\)

</td></tr><tr><td>

Closed Returned

</td><td>

Set when all returned lines have been processed and the return is complete.

</td><td>

Not applicable. This is the last state.

</td></tr><tr><td>

Closed Released

</td><td>

Set when the purchase order has been fully closed and released after successful fulfillment and payment.

</td><td>

Not applicable. This is the last state.

</td></tr><tr><td>

Closed Canceled

</td><td>

Set when the purchase order has been canceled and all active lines are in a canceled state.

</td><td>

Not applicable. This is the last state.

</td></tr></tbody>
</table>## Sourcing request states

The following table describes each sourcing request state, when the state is set, and where the sourcing request can move from that state. Sourcing request states reflect the current stage of the sourcing process, from initial review through supplier bid evaluation and award.

<table><thead><tr><th>

State

</th><th>

When this state is set

</th><th>

Next state

</th></tr></thead><tbody><tr><td>

Pending Review

</td><td>

Set when the sourcing request is first created. This is the initial state for all sourcing requests. Also re-entered when a purchase requisition line reverts to a pending review state, or when the primary line's approval cascades a pending review state to all other lines on the sourcing request.

</td><td>

-   Pending Approval
-   Information Needed

</td></tr><tr><td>

Pending Approval

</td><td>

Set when the sourcing request has been submitted for procurement manager approval and at least one purchase requisition line is awaiting approval.

</td><td>

-   Pending Review \(when approved and cascaded to lines\)
-   Closed Rejected \(when rejected\)

</td></tr><tr><td>

Information Needed

</td><td>

Set when the buyer requires more information from the requester before the sourcing request can proceed.

</td><td>

Pending Review \(when the required information is provided\)

</td></tr><tr><td>

Qualification Needed

</td><td>

Set when supplier or item qualification is required before bids can be solicited.

</td><td>

Qualified \(when qualification is complete\)

</td></tr><tr><td>

Qualified

</td><td>

Set when qualification is complete and the sourcing request is ready for negotiation setup. Also set when a negotiation event exists but not all negotiations have started.

</td><td>

Pending Negotiation

</td></tr><tr><td>

Pending Negotiation

</td><td>

Set when a negotiation event has been created for the sourcing request but has not yet opened for bidding.

</td><td>

Negotiation in Progress \(when the negotiation event opens\)

</td></tr><tr><td>

Negotiation in Progress

</td><td>

Set when a negotiation event is active and supplier bids are being collected. Also set when pricing has been obtained but a negotiation event is not yet fully completed.

</td><td>

-   Awaiting Supplier Response
-   Pending Resubmission

</td></tr><tr><td>

Pending Resubmission

</td><td>

Set when bids have been received but the negotiation event requires suppliers to resubmit revised bids.

</td><td>

Awaiting Supplier Response \(when the resubmission round closes\)

</td></tr><tr><td>

Awaiting Supplier Response

</td><td>

Set when the negotiation event has closed and the system is waiting for supplier bid responses to be evaluated.

</td><td>

-   Requires Decision
-   Closed No Decision

</td></tr><tr><td>

Awaiting Task Completion

</td><td>

Set when pricing has been obtained but one or more active sourcing-dependent procurement cases or purchasing tasks are still open against the sourcing request. The state is updated automatically when all blocking cases and tasks are closed.

</td><td>

Requires Decision \(when all blocking cases and tasks are closed\)

</td></tr><tr><td>

Requires Decision

</td><td>

Set when pricing has been obtained, no active negotiation event is blocking the sourcing request, and no open cases or tasks remain. A buyer decision is required to award or decline the sourcing.

</td><td>

-   Closed Complete \(when the award is accepted\)
-   Closed No Decision
-   Closed Canceled

</td></tr><tr><td>

Closed Complete

</td><td>

Set when the sourcing request has been awarded and closed. All pricing has been accepted and the sourcing outcome has been converted, typically to a purchase order.

</td><td>

Not applicable. This is the last state.

</td></tr><tr><td>

Closed No Decision

</td><td>

Set when the sourcing request is closed without a sourcing decision being made. All purchase requisition lines have reached a closed no decision state.

</td><td>

Not applicable. This is the last state.

</td></tr><tr><td>

Closed Canceled

</td><td>

Set when the sourcing request has been canceled. All active purchase requisition lines are in a canceled state.

</td><td>

Not applicable. This is the last state.

</td></tr><tr><td>

Closed Rejected

</td><td>

Set when all purchase requisition lines on the sourcing request have been rejected. When the primary line is rejected, all other lines on the sourcing request are also set to rejected.

</td><td>

Not applicable. This is the last state.

</td></tr></tbody>
</table>**Parent Topic:**[Sourcing and Procurement Operations reference](spo-reference.md)

**Related topics**  


[Base system procurement case type reference](base-system-procurement-case-types.md)

[Create New Pipeline Project form](create-pipeline-project-form.md)

[Pipeline project record tabs and UI actions](pipeline-form-tabs-actions.md)

[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

[Domain separation and Sourcing and Procurement Operations](../concept/psm-domain-separation.md)

[Sourcing and Procurement Operations glossary](../concept/spo-glossary.md#)

[Purchase requisition](purchase-requisition.md)

[Purchase order](purchase-order.md)

[Sourcing request](sourcing-request.md)

