---
title: Purchase order state model
description: The purchase order state model defines the happy-path sequence and deviation branches that a PO follows from creation to closure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-08-18"
reading_time_minutes: 5
keywords: [purchase order, state model, progress tracker, PO states]
breadcrumb: [Sourcing and Procurement Operations reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase order state model

The purchase order state model defines the happy-path sequence and deviation branches that a PO follows from creation to closure.

## Happy-path sequence

The standard path a PO follows from creation to payment closure.

-   Pending Submission
-   Ordered
-   Partially Delivered
-   Delivered
-   Payment Pending
-   Closed Paid

For punchout POs, two additional states are included:

-   Processing
-   Pending Supplier Confirmation
-   Pending Submission
-   Ordered
-   Partially Delivered
-   Delivered
-   Payment Pending
-   Closed Paid

\[Omitted image "progress-tracker-po-happy-path.png"\] Alt text: Purchase order record showing the Progress Tracker stepper with Pending Submission completed and Ordered as the current state.

## Deviation branches

Deviation branches for cases where a PO does not follow the happy path. Unlike the purchase requisition state model, purchase orders have three distinct deviation paths, each with its own terminal state.

|State|Description|
|-----|-----------|
|Pending Revision|The primary loop-back deviation. Rendered as a completed step before Pending Submission after the PO loops back through it, the same way Pending Revision renders on a purchase requisition.|
|Pending Return|Terminates at Closed Returned. A secondary, un-positioned deviation — unlike Pending Revision, this state is not rendered as a loop-back step in the happy-path sequence.|
|Pending Cancellation|Terminates at Closed Canceled. A secondary, un-positioned deviation, same as Pending Return.|
|Closed Released|An alternate, non-failure terminal — explicitly excluded from **negativeTerminals** in the configuration, unlike Closed Canceled and Closed Returned.|

\[Omitted image "progress-tracker-po-pending-revision.png"\] Alt text: Purchase order record showing Pending Revision rendered as a completed step before Pending Submission, with Ordered as the current state.

## State definitions

|State|Entry condition|
|-----|---------------|
|**Pending Submission**|The PO is created and awaits submission to the supplier.|
|**Ordered**|The PO is submitted to the supplier.|
|**Partially Delivered**|Some line items are delivered.|
|**Delivered**|All line items are delivered.|
|**Payment Pending**|Delivery is complete and the PO awaits payment processing.|
|**Closed Paid**|Payment is complete and the PO is closed. The happy-path terminal.|
|**Processing**|Punchout POs only. Precedes **Pending Supplier Confirmation** in the punchout variant happy path.|
|**Pending Supplier Confirmation**|Punchout POs only. The punchout order awaits the supplier's confirmation before moving to **Pending Submission**.|
|**Pending Revision**|The primary loop-back deviation. For entry conditions and terminal states, see [Deviation branches](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.md).|
|**Pending Return**|A secondary deviation that terminates at **Closed Returned**. For entry conditions and terminal states, see [Deviation branches](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.md).|
|**Pending Cancellation**|A secondary deviation that terminates at **Closed Canceled**. For entry conditions and terminal states, see [Deviation branches](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.md).|
|**Closed Released**|An alternate, non-failure terminal. For entry conditions and terminal states, see [Deviation branches](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.md).|
|**Closed Canceled**|A negative terminal reached from **Pending Cancellation**.|
|**Closed Returned**|A negative terminal reached from **Pending Return**.|

## State model differences

The PR and PO state models are distinct and not synchronized. A PR moves through approval and sourcing steps, while a PO moves through receipt and invoicing steps. The Progress Tracker renders different stepper paths for each record type. For the PR state model, see [Purchase requisition state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/pr-state-model.md). For related configuration, see [Configure PR and PO Progress Tracker states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-pr-po-states.md).

## Info card work items

For each PO state, the Progress Tracker info card displays different work items and assignment sources \(for example, receipt tasks, invoice tasks, procurement cases\). See [Progress Tracker component reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-info-card.md) for the complete field reference and state-specific content model.

**Parent Topic:**[Sourcing and Procurement Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/spo-reference.md)

**Related topics**  


[Base system procurement case type reference]()

[Create New Pipeline Project form]()

[Pipeline project record tabs and UI actions]()

[Savings opportunity fields]()

[Purchase requisition, purchase order, and sourcing request states]()

[Purchase requisition state model]()

[SPO and ITAM data model mappings]()

[Primary data tables for Sourcing and Procurement Operations]()

[Domain separation and Sourcing and Procurement Operations]()

[Sourcing and Procurement Operations glossary]()

[Address deletion permissions]()

