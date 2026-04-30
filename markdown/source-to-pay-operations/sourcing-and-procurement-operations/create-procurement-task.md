---
title: Create a procurement task
description: As a procurement specialist, create a procurement task for the shopper or employer from the contextual panel of a procurement object details page in Source-to-Pay Workspace, to address your procurement-related business needs.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Procurement Case Management, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create a procurement task

As a procurement specialist, create a procurement task for the shopper or employer from the contextual panel of a procurement object details page in Source-to-Pay Workspace, to address your procurement-related business needs.

Describes the procedure for creating a procurement task from the Procurement workspace. 

## Before you begin

Role required: sn\_shop.procurement\_specialist

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Procurement Workspace**.

2.  On the list page, navigate to **All work**.

3.  Do one of the following:

<table><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

To create a procurement task for a procurement case.

</td><td>

1.  Select **Cases**.
2.  Select the link to the procurement case record under the Number column.
3.  On the **Purchasing Tasks** tab, select **New**.


</td></tr><tr><td>

To create a procurement task for the other procurement objects.

</td><td>

1.  Select any of the following modules and select the link to the record under the Number column.
    -   **Sourcing request**
    -   **Sourcing event**
    -   **Negotiation**
    -   **Purchase requisition**
2.  Select the link to the record under the Number column to open it.
3.  Select **Related work** &gt; **Purchasing Tasks**.
4.  Select **New**.


</td></tr></tbody>
</table>4.  On the Create new task dialog box, select **Procurement task** from the **Task type** list.

5.  Select **Submit**.

6.  On the form, fill in the fields.

<table id="table_ecv_33n_2wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier for the task.

</td></tr><tr><td>

Task type

</td><td>

Type of task based on the requirement.

</td></tr><tr><td>

Action type for task

</td><td>

Type of action that the shopper must complete for this task to progress. The options are:-   Mark complete
-   View link
-   Play video
-   Upload documents
-   Complete a form
-   Sign document
**Note:**

-   For View link or Play video action types, the required **URL** field must be populated with the desired link.
-   For the Complete a form action type, the required **Catalog item** field must be populated with the desired form or catalog item that is to be completed.
-   For the Sign document action type, the required **Document template** field must be populated with the desired preconfigured template that is to be sent for signing.


</td></tr><tr><td>

Assignment group

</td><td>

Group to which the task is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

Person within the assignment group to whom the task is assigned to.**Note:** You must assign the action type to the concerned shopper or employee for them to find it in their tasks list.

</td></tr><tr><td>

State

</td><td>

Current state the task is in.**Note:** The assigned to shopper or employee can view this task in Employee Center or Shopping Hub only when the status of the task is updated to Work in Progress.

</td></tr><tr><td>

Due date

</td><td>

Expected date and time by when the task is expected to be resolved.

</td></tr><tr><td>

Sourcing decision dependent on task

</td><td>

Whether any sourcing decision is dependent on the task.**Note:** This field is displayed only if a related sourcing request is entered.​

</td></tr><tr><td>

Qualification dependent on task

</td><td>

Whether any qualification is dependent on the task.**Note:** This field is displayed only if a related sourcing request is entered.​

</td></tr><tr><td>

Order dependent on task

</td><td>

Whether the order is dependent on the task.**Note:** This field is displayed only if a related purchase requisition is entered.​

</td></tr><tr><td>

Short description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Related case

</td><td>

Case associated with the task.

</td></tr><tr><td>

Sourcing request

</td><td>

Sourcing request associated with the task.

</td></tr><tr><td>

Purchase requisition

</td><td>

Purchase requisition associated with the task.

</td></tr><tr><td>

Purchase order

</td><td>

Purchase order associated with the task.

</td></tr><tr><td>

Expected start

</td><td>

Date and time by when work is expected to start on the task.

</td></tr><tr><td>

Actual start

</td><td>

Date and time when work actually starts on the task.

</td></tr><tr><td>

Actual end

</td><td>

Date and time when work actually completes on the task.

</td></tr><tr><td>

Duration

</td><td>

Time taken to resolve the task, in days, hours, minutes, and seconds.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  Select **Send to assignee** to send the task to the assigned shopper or employee's queue.

    If you have created a procurement task with action type as Sign document, a document task is automatically created and assigned to the selected shopper or employee.


**Parent Topic:**[Using Procurement Case Management](../concept/using-pcm.md)

