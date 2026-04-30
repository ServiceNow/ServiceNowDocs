---
title: Purchasing tasks and procurement cases
description: All automated purchasing tasks and procurement cases are created using flow designer from the Service Delivery Common \(SDC\) application. The flow designer uses the underlying task and case generation decision tables. Purchasing tasks and procurement cases are created based on the conditions defined in the decision tables.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [automatically create purchasing tasks, automatically create procurement cases]
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchasing tasks and procurement cases

All automated purchasing tasks and procurement cases are created using flow designer from the Service Delivery Common \(SDC\) application. The flow designer uses the underlying task and case generation decision tables. Purchasing tasks and procurement cases are created based on the conditions defined in the decision tables.

## Conditions and triggers for task and case creation

The **Sourcing decision dependent on case** and **Order dependent on case** fields in the Finance Case table determine the need for a [procurement case](../concept/spo-glossary.md#) to be created. In contrast, the **Sourcing decision dependent on task** and **Order dependent on task** fields in the Finance Task table determine the need for a [procurement task](../concept/spo-glossary.md#) to be created.

Tasks and cases are generated when the following rules are triggered. The decision tables support this generation via decision inputs.

-   Purchase Requisition Task and Case Generation Rule
-   Sourcing Request Task and Case Generation Rule
-   Negotiation Task and Case Generation Rule
-   Sourcing Event Task and Case Generation Rule

## Procurement case types

Here’s a list of the types and subtypes of procurement cases:

-   Edit a purchase
-   Edit a receipt
-   GL Coding Review
-   Budget Review
-   Contract Review
-   Send NDA for Signature
-   Return a purchase
-   Replace a purchase
-   Request a Corporate Card
-   Inquiry
-   Delivery Address Review
-   Request a copy of contract
-   Due Diligence

For procurement cases, you can also create child cases or associate child cases to parent cases. However, remember that you must close all child cases and associated child cases before you can close any parent case. Similarly, you can reopen a child case or associated child case only when the parent case is still open.

## Procurement case states

The states that are available for a procurement case are listed.

-   Draft
-   Processing Case
-   In Review
-   On Hold
-   Work in Progress
-   Closed Canceled
-   Closed Rejected
-   Closed Completed
-   Awaiting Acceptance

When the condition in the **Enable case resolution acceptance** decision table is set to **True**, the procurement case state automatically changes to Awaiting Acceptance after the fulfiller sets it to Closed Completed.

The requestor gets an email notification to accept or reject the resolution within a set time.

-   If the requestor accepts the case resolution, a predefined email is generated for them to send and the case automatically changes to Closed Completed.
-   If the requestor rejects the case resolution, the case moves back to Work in Progress.
-   If the requestor does not respond in time, the case is automatically marked as Closed Completed.

For more information on email notifications, see [Alerts and email notifications from ShoppingHub](alerts-messages-email-notifications.md#awaiting_acceptance_email_notification).

## Purchasing task types

Here's a list of the types and subtypes of purchasing tasks:

-   Purchasing task
    -   Select a Supplier: Ask the shopper to compare pricing from multiple suppliers and select a supplier.
    -   Sourcing task
    -   Ask a question: Ask the shopper for more information about the purchase.
-   Procurement/Supplier task: Create a procurement task for a supplier.

![Create new procurement task.](../image/create_procurement_task.png)

You can also create child tasks or associate child tasks to parent tasks. However, you must close all child tasks and associated child tasks before you can close any parent task. Similarly, you can reopen a child task or associated child task only when the parent task is still open.

The following are the key fields of a purchasing task:

<table id="table_v3k_j25_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the purchasing task.

</td></tr><tr><td>

Assignment group

</td><td>

Group to which this purchasing task belongs.

</td></tr><tr><td>

Assigned to

</td><td>

User to which this purchasing task is assigned.

</td></tr><tr><td>

Primary contact

</td><td>

Person within the procurement team working on the purchase who can be contacted with questions. This field is populated or updated with the same user in the **Assigned to** field of the parent task record, as follows:-   For a sourcing task, from the referenced sourcing request
-   For a purchasing task, from the purchasing task itself
-   For a contract task, from the contract task itself
-   For a supplier task, from the supplier task itself
-   For a finance task, from the finance task itself

</td></tr><tr><td>

State

</td><td>

Status of the purchasing task.

</td></tr><tr><td>

Substate

</td><td>

Progress of obtaining the shopper’s responses to the procurement specialist’s questions.

</td></tr><tr><td>

Due date

</td><td>

Expected date of completing the task.

</td></tr><tr><td>

Short description

</td><td>

Short description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td>

Detailed description

</td><td>

Detailed description of the Custom Task for Employee task subtype. You can enter your instructions in HTML or rich text format. You can add hyperlinks or images as required.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Supplier

</td><td>

Supplier reference for this task.

</td></tr><tr><td>

Sourcing request

</td><td>

Sourcing request associated with this task.

</td></tr><tr><td>

Purchase requisition

</td><td>

Purchase requisition associated with this task.

</td></tr><tr><td>

Purchase order

</td><td>

Purchase order for which the revision request task is raised.

</td></tr><tr><td>

Sourcing decision dependent on task

</td><td>

Specifies whether this task must be completed before a sourcing request can be created.**Note:** This field is displayed only if a related sourcing request is entered.​

</td></tr><tr><td>

Qualification dependent on task

</td><td>

Specifies whether this task must be completed before a qualification request can be created.**Note:** This field is displayed only if a related sourcing request is entered.​

</td></tr><tr><td>

Order dependent on task

</td><td>

Determines if completion of this task is required prior to a purchase order being created.**Note:** This field is displayed only if a related purchase requisition is entered.​

</td></tr><tr><td>

Expected start

</td><td>

Expected date of starting work on the task.

</td></tr><tr><td>

Actual start

</td><td>

Actual date of starting work on the task.

</td></tr><tr><td>

Actual end

</td><td>

Actual date of completing the task.

</td></tr><tr><td>

Duration

</td><td>

Actual time taken to complete the task.

</td></tr><tr><td class="sub-head" colspan="2">

Question &amp; Answer

</td></tr><tr><td colspan="2">

This section contains the information of the questions posed to the shopper and the responses that the shopper provides.

</td></tr></tbody>
</table>-   **[Purchasing task and procurement case creation](../concept/automated-purchasing-task-creation-from-flow-designer.md)**  
Create purchasing tasks and procurement cases in sourcing requests and purchase requisitions.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

