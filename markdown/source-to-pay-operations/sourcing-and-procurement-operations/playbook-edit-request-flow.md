---
title: Process a purchase requisition edit request in playbook
description: Use the procurement playbook to approve or reject the revision requests for the quantity of the product or delivery location.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Process a purchase requisition edit request in playbook

Use the procurement playbook to approve or reject the revision requests for the quantity of the product or delivery location.

## Before you begin

Role required: sn\_spend\_psd.admin, agents, fulfillers

## About this task

As an agent, you can view the requests, complete tasks across multiple workflow activities, and manage complex operations from a unified playbook. The playbook provides agents an automated way to visualize the overall process in a task-oriented format.

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select **All work** &gt; **Cases**.

3.  Select a case of type **Edit a purchase**.

    **Note:** With the revision request raised, the state has been changed to Pending Revision for both the purchase requisition and purchase line. Remember that the **Edit** option is unavailable for purchases in the Close state. You can view all the associated information in the **Details** tab, and information on the procurement case lines, tasks, and original purchase in the **Procurement Case Lines**, **Purchasing Tasks**, **Related work**, and **Original purchase** tabs.

    The **Playbook** tab opens with the **Edit a purchase requisition** section.

4.  Complete the steps in the various stages and activities of the Edit a purchase requisition playbook.

<table id="table_bgd_tzx_ztb"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

Review case

</td><td>

Assign case

</td><td>

Use this activity to assign the case to a different person or keep the case assigned to you.You can do the following:

 -   In the **Assigned to** search field, search for and select the person that you want to assign the case to.
-   In the **Short description** field, update the description for the case.
-   Select one of the following actions:
    -   Select **Save** to save your changes.
    -   Select **Start work** to start working on the case.


</td></tr><tr><td rowspan="2">

Intake and Assess

</td><td>

Modifications requested by shopper

</td><td>

This activity completes automatically.

</td></tr><tr><td>

Confirm or reject request to edit PR

</td><td>

This activity enables you to review the initial request, confirm or reject the request to edit the PR. The available options are:-   **Confirm**: When you confirm, you can check the revised the purchase request or purchase request line with updated quantity and location. On successful update, the request to edit a purchase request is automatically closed.
-   **Reject**: When you reject, you must contact the supplier and confirm whether the order can be rejected. When a supplier allows cancellation, the request changes to Closed Rejected state.


</td></tr><tr><td>

Process PR Edit

</td><td>

Update PR with new details

</td><td>

This activity updates the PR with new details and completes automatically.

</td></tr><tr><td rowspan="3">

Close case

</td><td>

Notify the requestor

</td><td>

Use this activity to email the business owner confirming that lines from their purchase requisition have been successfully edited.

 A draft email appears with pre-populated data in the **Subject** field. The email body is pre-populated with the relevant text.

 Select **Send Email** to send the email.

</td></tr><tr><td>

Complete case

</td><td>

Use this activity to add work notes and close the case.

Do the following:

-   In the **Work notes** field, add any comments about the case.
-   In the **Close notes** field, add any closing comments.
-   Select **Complete case**.
Updates the case to Closed Completed.

</td></tr><tr><td>

Update case to complete

</td><td>

After the PR has been updated, the request to edit a PR is automatically closed.

</td></tr></tbody>
</table>
## Result

The request updates the purchase requisition or line item with revised quantity or location. A new card of revision type is also created for the shopper and approvers to communicate on, which can be viewed by the shopper from **My purchases**.

**Parent Topic:**[Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace](../concept/work-playbooks-spo.md)

**Related topics**  


[Process a purchase order edit in playbook](process-purchase-order.md)

[Process a return request in playbook](playbook-return-request.md)

[Process a replacement request in playbook](playbook-replacement-request.md)

[Process an edit receipt request in playbook](playbook-process-edit-receipt.md)

[Fulfilling request for copy of contract in playbook](../concept/fulfilling-request-for-contract.md)

[Routing NDAs to suppliers](../concept/routing-ndas-to-suppliers.md)

[Verifying delivery addresses in playbook](../concept/delivery-address-in-playbook.md)

[Reviewing and updating general ledger details in playbook](../concept/general-ledger-details-in-playbook.md)

[Sourcing intake guided experience with playbooks](../concept/sourcing-intake-guided-exp.md)

[Streamlining the supplier risk assessment workflow](../concept/simplify-risk-assessment-wf.md)

[Purchase revision flows](../concept/purchase-revision-flows.md)

[Purchase revision roles and responsibilities](../concept/purchase-revision-flows-roles.md)

[Playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

