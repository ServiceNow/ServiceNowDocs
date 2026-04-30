---
title: Work on a group life policy service case
description: Work on a group life case to change or review member information, and complete the policy service request.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Group Life Servicing, Group Life Servicing, Life Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Work on a group life policy service case

Work on a group life case to change or review member information, and complete the policy service request.

## Before you begin

Role required: sn\_ins\_group\_life.processor, sn\_ins\_group\_life.contributor, or sn\_ins\_group\_life.processor\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a customer requires an insurance policy change, a Group life contributor, such as a relationship manager, initiates a case and updates its details, triggering the workflow. Throughout the workflow, insurance and document agents complete their assigned tasks and update the status of the case.

**Note:** Depending on the policy service request type, a workflow might have additional or fewer tasks.

Use the case playbook that provides the activities and tasks required to research and complete the request.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../../fso-card-operations/image/list-icon.png)\).

3.  In the **Lists** tab, under **Group life service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all Group life cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

    The case playbook guides processors through the steps that are involved in resolving a case.

6.  Use the activities and tasks under the following playbook stages to fulfill the request and resolve the case:

    -   **Initiate and review** to enter policy details or coverage changes, collect customer documents, and submit the case for review.
    -   **Processor review** to verify customer documents, review policy details, and submit the review.
    -   **Customer acceptance** to update with the customer's decision to accept or reject the quote.
    -   **Fulfillment** to activate the accepted change, update the policy record, send updated policy documents to the customer, and close the case.
    Any tasks generated during playbook activities appear in the **Tasks** tab of the case.

7.  In the **Work notes** field, enter any comments.

8.  Close the task from the playbook activity or the task form.

<table><thead><tr><th align="left" id="d94041e230">

Policy task

</th><th align="left" id="d94041e233">

Action

</th></tr></thead><tbody><tr><td id="d94041e239">

**To verify a change or a document**

</td><td>

-   In the case playbook, click **Mark complete**.
-   In the task form, in the **State** field, change the state of the task to **Closed Complete**.


</td></tr><tr><td id="d94041e266">

**To submit a review**

</td><td>

Select **Approve** to approve or **Reject** to reject the request.

</td></tr></tbody>
</table>
## Result

The case automatically updates to show Closed Complete.

