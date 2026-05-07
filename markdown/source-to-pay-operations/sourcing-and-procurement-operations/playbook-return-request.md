---
title: Process a return request in playbook
description: Use the procurement playbook to approve or reject return requests.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Working with playbooks, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Process a return request in playbook

Use the procurement playbook to approve or reject return requests.

## Before you begin

Role required: sn\_spend\_psd.admin, agents, fulfillers

## About this task

As an agent, you can view the requests, complete tasks across multiple workflow activities, and manage complex operations from a unified playbook. The playbook provides agents an automated way to visualize the overall process in a task-oriented format.

![Process a return request in playbook](../image/pb-return-purchase.png)

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select **All work** &gt; **Cases**.

3.  Select the request number from the list for further processing.

4.  Complete the steps in the various stages and activities of the Return a purchase playbook.

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

Use this activity to assign the case to a different person or keep the case assigned to you.In the **Assigned to** search field, select a procurement specialist to work on this case.

Select one of the following actions:

-   Select **Save** to save your changes.
-   Select **Start work** to start working on the case.


</td></tr><tr><td rowspan="2">

Intake and Assess

</td><td>

Lookup procurement case lines

</td><td>

Look up procurement case line associated with this return request for use later in the process.

</td></tr><tr><td>

Assign return request

</td><td>

Return request is automatically assigned to the buyer assigned to the original purchase.

</td></tr><tr><td rowspan="3">

Coordinate with Supplier

</td><td>

Confirm return and collect information

</td><td>

Contact the supplier, confirm the return, and collect the necessary information.Select to verify and process the information about the request.

-   **Confirm**: After you verify that return is feasible, confirm the request. When confirmed, the request moves to the Work in progress state. You can now send an email to the business owner confirming that the return request has been initiated.
-   **Reject**: When you reject the return request, the request moves to the Closed Rejected state. You can now close the case by sending an email to the business owner confirming that the return request has been rejected.


</td></tr><tr><td>

Get POLs from Service Case

</td><td>

Updates state of Purchase Order Lines to pending return.

</td></tr><tr><td>

Send business owner email confirming return

</td><td>

Sends the business owner confirmation that after reviewing the return and coordinating with supplier, the return is feasible.

</td></tr><tr><td rowspan="3">

Reverse Goods Receipt

</td><td>

Reverse goods receipt

</td><td>

Creates a receipt type for the goods that are to be shipped back to the supplier. This receipt is recorded on the purchase order record. If you skip this step, the request moves to the Closed Rejected state. You can then close the case by sending an email to the business owner confirming that the return request has been rejected.

</td></tr><tr><td>

Create return

</td><td>

Creates a receipt of type return.

</td></tr><tr><td>

Set POL status after return

</td><td>

Updates the POL status to appropriate state based on the Returned and Accepted quantities.

</td></tr><tr><td rowspan="3">

Create Debit Memo

</td><td>

Create Debit Memo / Skip

</td><td>

Creates a debit memo invoice for this return. This debit memo is recorded on the purchase order record. If the invoice for these returned goods is yet to be paid, a debit memo isn’t required. You may choose to skip this step, if required.

</td></tr><tr><td>

Create invoice of type debit memo

</td><td>

Creates a debit memo.

</td></tr><tr><td>

Create invoice line for debit memo

</td><td>

Creates an invoice line associated with debit memo in Shopping Hub.

</td></tr><tr><td rowspan="4">

Close case

</td><td>

Retire Assets

</td><td>

Any associated assets or fixed assets created during purchase order creation are revised based on the quantity of the returned products. The states of these assets and fixed assets are updated to Retired and Pending Deletion respectively.

</td></tr><tr><td>

Send business owner email confirming successful return

</td><td>

Sends the business owner confirmation that their return has been processed successfully.

</td></tr><tr><td>

Complete case

</td><td>

Use this activity to add work notes and close the case.

 Do the following:

-   In the **Work notes** field, add any comments about the case.
-   In the **Close notes** field, add any closing comments.
-   Select **Complete case**.


</td></tr><tr><td>

Update case to complete

</td><td>

Updates the case to Closed Completed.

</td></tr></tbody>
</table>
**Parent Topic:**[Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace](../concept/work-playbooks-spo.md)

**Related topics**  


[Process a purchase order edit in playbook](process-purchase-order.md)

[Process a purchase requisition edit request in playbook](playbook-edit-request-flow.md)

[Process a replacement request in playbook](playbook-replacement-request.md)

[Process an edit receipt request in playbook](playbook-process-edit-receipt.md)

[Fulfilling request for copy of contract in playbook](../concept/fulfilling-request-for-contract.md)

[Routing NDAs to suppliers](../concept/routing-ndas-to-suppliers.md)

[Verifying delivery addresses in playbook](../concept/delivery-address-in-playbook.md)

[Reviewing and updating general ledger details in playbook](../concept/general-ledger-details-in-playbook.md)

[Sourcing intake guided experience with playbooks](../concept/sourcing-intake-guided-exp.md)

[Streamlining the supplier risk assessment workflow](../concept/simplify-risk-assessment-wf.md)

