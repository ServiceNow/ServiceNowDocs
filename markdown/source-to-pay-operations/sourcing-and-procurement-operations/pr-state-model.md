---
title: Purchase requisition state model
description: Reference for the complete purchase requisition \(PR\) state model, including the standard progression sequence and alternative progression branches that a PR can follow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/pr-state-model.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-08-18"
reading_time_minutes: 5
breadcrumb: [Sourcing and Procurement Operations reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase requisition state model

Reference for the complete purchase requisition \(PR\) state model, including the standard progression sequence and alternative progression branches that a PR can follow.

## Happy-path sequence

The standard path a PR follows from creation to closure.

-   Pending Review
-   Pending Approval
-   Awaiting Task Completion
-   Final Review
-   Pending Submission
-   Closed Complete

For punchout PRs, the sequence includes an additional state:

-   Pending Review
-   Pending Approval
-   Awaiting Task Completion
-   Final Review
-   Pending Supplier Confirmation
-   Pending Submission
-   Closed Complete

\[Omitted image "progress-tracker-pr-happy-path.png"\] Alt text: Progress Tracker stepper showing six sequential states from Pending Review to Closed Complete

## Deviation branches

Deviation branches for cases where a PR does not follow the happy path.

|State|Description|
|-----|-----------|
|Pending Revision|Entered from Pending Review or Pending Approval when an approver rejects the PR because it does not meet requirements. From Pending Revision, the PR can loop back to Pending Review once the requestor makes the required changes.|
|Closed Rejected|A terminal state reached from Pending Review, Pending Approval, or Final Review when the PR is rejected. The PR cannot transition out of Closed Rejected.|
|Closed Canceled|A terminal state reached from multiple points when the PR is canceled. The PR cannot transition out of Closed Canceled. The underlying test suite covers both a buyer-initiated and a shopper-initiated cancellation path. Both terminate at Closed Canceled. The tracker does not currently distinguish who canceled the PR.|
|Pending Cancellation|Not modeled as a distinct state on purchase requisitions. A PR that is canceled transitions directly to Closed Canceled with no intermediate "pending" step. The purchase order state model does define a distinct Pending Cancellation alternative progression. For details, see [Purchase order state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.md).|
|Pending Supplier Confirmation|Punchout PRs only. This state is part of the punchout variant standard progression. The state is entered after Final Review and before Pending Submission. The PR waits for the supplier to confirm the punchout order.|

Each step in the stepper payload carries one of four status values: `done`, `current`, `upcoming`, or `terminal_negative` \(used for Closed Rejected and Closed Canceled\).

\[Omitted image "progress-tracker-pr-pending-revision.png"\] Alt text: Progress Tracker stepper displaying Pending Revision deviation state with alert banner

## State definitions

|State|Entered when…|
|-----|-------------|
|Pending Review|The PR is created and awaits initial review.|
|Pending Approval|Initial review is complete and the PR is routed to approvers.|
|Awaiting Task Completion|Approval is granted and fulfiller tasks \(for example, source creation, contract review\) are generated.|
|Final Review|All fulfiller tasks are complete and the PR awaits final acceptance.|
|Pending Submission|Final review is passed and the PR is ready to be submitted to the supplier \(for example, as a PO or punchout flow\).|
|Closed Complete|The PR has been submitted and all post-submission tasks \(receipt, invoicing\) are complete.|
|Pending Revision|An approver has rejected the PR, requiring rework.|
|Closed Rejected|An approver has rejected the PR at a stage where rejection is terminal \(no further revision is allowed\).|
|Closed Canceled|The PR has been canceled by a system administrator or authorized user.|
|Pending Supplier Confirmation|Punchout PRs only. The punchout order has passed Final Review and is awaiting the supplier's confirmation before moving to Pending Submission.|
|Pending Cancellation|Not modeled for purchase requisitions. A canceled PR goes directly to Closed Canceled. This is a purchase order-only alternative progression. For details, see [Purchase order state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.md).|

## Info card and work items

For each PR state, the Progress Tracker info card displays different work items and assignment sources. For the complete field reference and state-specific content, see [Progress Tracker component reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-info-card.md).

**Parent Topic:**[Sourcing and Procurement Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/spo-reference.md)

**Related topics**  


[Base system procurement case type reference]()

[Create New Pipeline Project form]()

[Pipeline project record tabs and UI actions]()

[Savings opportunity fields]()

[Purchase requisition, purchase order, and sourcing request states]()

[Purchase order state model]()

[SPO and ITAM data model mappings]()

[Primary data tables for Sourcing and Procurement Operations]()

[Domain separation and Sourcing and Procurement Operations]()

[Sourcing and Procurement Operations glossary]()

[Address deletion permissions]()

