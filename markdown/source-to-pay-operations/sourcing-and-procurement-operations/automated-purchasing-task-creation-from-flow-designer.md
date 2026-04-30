---
title: Purchasing task and procurement case creation
description: Create purchasing tasks and procurement cases in sourcing requests and purchase requisitions.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Purchasing tasks and procurement cases, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchasing task and procurement case creation

Create purchasing tasks and procurement cases in sourcing requests and purchase requisitions.

## Sourcing request

If a negotiation does not exist, the supplier risk assessment and send NDA for signature cases are triggered when the state of the sourcing request is Awaiting Supplier Response. The procurement cases are created on the cases related list of the sourcing request.

-   Conduct a supplier risk assessment: If risk assessment on the referenced supplier record is not valid, create a supplier risk assessment case for each supplier on the sourcing request.
-   Send NDA for signature: If the NDA on the referenced supplier record is not valid, create an NDA case for each supplier on the sourcing request. This requires adding a supplier reference field on the case template.
-   If the user skips updating the state of the sourcing request to Awaiting Supplier Response, these cases are created when the state of the sourcing request is Requires Decision.
-   If the user decides to manually create contracts against the sourcing request, trigger the contract review case once a contract is created.

If a new supplier is added to the sourcing request, the risk assessment and send NDA for signature cases for that supplier are triggered when the state of the sourcing request is Awaiting Supplier Response or Requires Decision \(if the user skipped the Awaiting Supplier Response state\).

Purchasing tasks and procurement cases for the awarded supplier that are created on a sourcing request are also shown on the purchase requisition.

For information on how a supplier tiering assessment case influences sourcing request states, see [Sourcing and Procurement Operations integration with Third-party Risk Management](better-together-with-vrm.md).

## Purchase requisition

The following procurement cases and purchasing tasks are created in flow designer when the state of the purchase requisition is Pending Review or Pending Approval \(if approvals are triggered\):

-   Cases:
    -   GL coding review
    -   Budget review
    -   Conduct a supplier risk assessment
    -   Onboard a supplier
    -   Send NDA for signature
    -   Delivery address verification \(not applicable for blanket order type scenario\)
    -   Delivery address approval \(not applicable for blanket order type scenario\)
-   Tasks: Follow up required: Approval duration breached

The integration error purchasing task is created in flow designer when integration with ERP fails and the state of the purchase requisition is updated to Awaiting Task Completion.

If a purchase requisition is created directly without a sourcing request, all purchasing tasks and procurement cases are created in flow designer when the state of the purchase requisition is Pending Review or Pending Approval \(if approvals are triggered\), with the exception of contract review case and integration error task. These are created when the state is Awaiting Task Completion. If the tasks and cases triggered during the Pending Review or Pending Approval state are still open after approvals are complete, the state of the purchase requisition is in Awaiting Task Completion. Only when all the **Order dependent on task** tasks and **Order dependent on case** cases are closed, the state of the purchase requisition is updated to Final Review or PO Created, based on the purchasing property.

**Parent Topic:**[Purchasing tasks and procurement cases](../reference/purchasing-tasks.md)

