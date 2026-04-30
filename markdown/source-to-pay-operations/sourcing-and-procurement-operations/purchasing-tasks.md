---
title: Purchasing tasks and procurement cases
description: All automated purchasing tasks and procurement cases are created using flow designer from the Service Delivery Common \(SDC\) application. Flow designer uses the underlying task and case generation decision tables, and purchasing tasks and procurement cases are created based on the conditions defined in the decision tables.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchasing tasks and procurement cases

All automated purchasing tasks and procurement cases are created using flow designer from the Service Delivery Common \(SDC\) application. Flow designer uses the underlying task and case generation decision tables, and purchasing tasks and procurement cases are created based on the conditions defined in the decision tables.

## Conditions and triggers for task and case creation

While the **Sourcing decision dependent on case** and **Order dependent on case** fields in the Service Case table determine the need for a procurement case to be created, the **Sourcing decision dependent on task** and **Order dependent on task** fields in the Service Task table determine the need for a procurement task to be created.

Tasks and cases are generated when the following rules are triggered, with the decision tables supporting this generation via decision inputs.

-   Purchase Requisition Task and Case Generation Rule
-   Sourcing Request Task and Case Generation Rule
-   Negotiation Task and Case Generation Rule
-   Negotiation Event Task and Case Generation Rule

## Procurement case types

Here’s a list of the types and subtypes of procurement cases:

-   Supplier cases:

    -   Conduct a Supplier Risk Assessment: Conduct a risk assessment for a supplier.
    -   Onboard a Supplier: Onboard a supplier for a purchase.
    -   Conduct a Supplier Tiering Assessment: Conduct a tiering assessment for a supplier.
    **Note:** For these supplier cases, the decision templates are available only when you have the Supplier Lifecycle Operations application installed. You must also enable the Risk Assessments Integration for Sourcing and Procurement Operations application and have the GRC Vendor Risk Management license if you want the Conduct a Supplier Tiering Assessment case to be generated. For information on how a supplier tiering assessment task influences sourcing request states, see [Sourcing and Procurement Operations integration with Third-party Risk Management](../concept/better-together-with-vrm.md).

-   Contract cases​:
    -   Contract Review: Review contracts for a purchase.
    -   Send NDA for Signature: Send an NDA for signature to the supplier for a purchase.
-   Finance cases​:
    -   GL Coding Review: Review accounting details for a purchase line.
    -   Budget Review: Review budget details for a purchase requisition.
-   Delivery Address Review

For procurement cases, you can also create child cases or associate child cases to parent cases. However, remember that you must close all child cases and associated child cases before you can close any parent case. Similarly, you can reopen a child case or associated child case only when the parent case is still open.

## Procurement case states

The default states that are available for a procurement case are listed.

-   Draft
-   Processing Case
-   In Review
-   On Hold
-   Work in Progress
-   Closed Canceled
-   Closed Rejected
-   Closed Completed

## Purchasing task types

A list of the types and subtypes of purchasing tasks are listed below.

-   Purchasing task
    -   Select a Supplier: Ask the shopper to compare pricing from multiple suppliers and select a supplier.
    -   Sourcing task
    -   Ask a question: Ask the shopper for more information about the purchase.
-   Procurement/Supplier task: Create a procurement task for a supplier.

You can also create child tasks or associate child tasks to parent tasks. However, remember that you must close all child tasks and associated child tasks before you can close any parent task. Similarly, you can reopen a child task or associated child task only when the parent task is still open.

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

Progress of obtaining answers from the shopper to the questions of the procurement specialist.

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

Detailed description of the task. This is specific to the Custom Task for Employee task subtype, where you can enter your instructions in html or rich text format, and even add hyperlinks or images as required.

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

Determines if completion of this task is required prior to a sourcing request being created.**Note:** This field is displayed only if a related sourcing request is entered.​

</td></tr><tr><td>

Qualification dependent on task

</td><td>

Determines if completion of this task is required prior to a qualification request being created.**Note:** This field is displayed only if a related sourcing request is entered.​

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

