---
title: Process a purchase order edit in playbook
description: You can edit and revise the quantity of the product or delivery location of the purchase orders based on your requirements.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Working with playbooks, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Process a purchase order edit in playbook

You can edit and revise the quantity of the product or delivery location of the purchase orders based on your requirements.

## Before you begin

Role required: sn\_spend\_psd.requestor, administrator

## About this task

As an agent, you can view the requests, complete tasks across multiple workflow activities, and manage complex operations from a unified playbook. The [playbook](../concept/spo-glossary.md#) provides agents an automated way to visualize the overall process in a task-oriented format.

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select **All work** &gt; **Cases**.

3.  Select the case of type Edit a purchase order.

    **Note:** With the revision request raised, the state has been changed to Pending Revision for both the purchase order and purchase order line. Remember that the **Edit** option is unavailable for purchases in the Close state.

4.  Complete the steps in the various stages and activities of the Edit a purchase order playbook.

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

Lookup procurement case line

</td><td>

This activity provides more information on the service request, purchase request, and purchase request line items.Select **Details about changes to this purchase** to review the changes.

</td></tr><tr><td>

Buyer confirm or reject request to edit PO

</td><td>

Review this request to edit the purchase order and confirm or reject whether it can be processed.Select one of the following actions.

-   **Confirm**: When you confirm, you can check the revised the purchase order or purchase order line. On successful update, the request is automatically closed.
-   **Reject**: When you reject, you must contact the supplier and confirm whether the order can be rejected. When the supplier allows cancellation, the request changes to Closed Rejected state.


</td></tr><tr><td rowspan="2">

Process PO Edit

</td><td>

Update POLs to pending revision state

</td><td>

Updates the POLs state to pending revision until the PR of type revision is approved and the PO is updated.

</td></tr><tr><td>

Create PR of type Revision

</td><td>

Creates a PR of type revision with the Shopper's changes to the PO.

</td></tr><tr><td rowspan="3">

Close case

</td><td>

Send business owner confirmation email

</td><td>

Sends the business owner confirmation that lines from their purchase order have been successfully edited using Shopping Hub email template.

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

After the PO has been updated, the request to edit the purchase order is automatically closed.

</td></tr></tbody>
</table>
## Result

The request updates the purchase order or line item with revised quantity, location, delivery dates, or service dates. A new card of revision type is also created for the shopper and approvers to communicate on, which can be viewed by the shopper from **My purchases**.

## What to do next

Review and confirm your purchase request details from **Procurement Case Management** &gt; **Procurement Cases** &gt; **Purchase Requisitions** &gt; **Purchase lines**, if required.

**Parent Topic:**[Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace](../concept/work-playbooks-spo.md)

**Related topics**  


[Process a purchase requisition edit request in playbook](playbook-edit-request-flow.md)

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

[Playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

