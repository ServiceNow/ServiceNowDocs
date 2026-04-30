---
title: Process a replacement request in playbook
description: Use the procurement playbook to approve or reject replacement requests.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Process a replacement request in playbook

Use the procurement playbook to approve or reject replacement requests.

## Before you begin

Role required: sn\_spend\_psd.admin, agents, fulfillers

## About this task

As an agent, you can view the requests, complete tasks across multiple workflow activities, and manage complex operations from a unified playbook. The playbook provides agents an automated way to visualize the overall process in a task-oriented format.

![Process a replacement request in playbook](../image/pb-replacement-purchase.png)

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select **All work** &gt; **Cases**.

3.  Select the Replace a purchase case from the list for further processing.

4.  Complete the steps in the various stages and activities of the Replace a purchase playbook.

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

Look up procurement case line associated with this replacement request for use later in the process.

</td></tr><tr><td>

Assign replacement request

</td><td>

Replacement request is automatically assigned to the buyer assigned to the original purchase.

</td></tr><tr><td rowspan="2">

Coordinate with Supplier

</td><td>

Confirm replacement and collect information

</td><td>

Contact the supplier, confirm the replacement, and collect the necessary information.Select to verify and process the information about the request.

-   **Confirm**: After you verify that replacement is feasible, confirm the request. When confirmed, the request moves to the Work in progress state. You can now send an email to the business owner confirming that the replacement request has been initiated.
-   **Reject**: When you reject the replacement request, the request moves to the Closed Rejected state. You can now close the case by sending an email to the business owner confirming that the replacement request has been rejected.


</td></tr><tr><td>

Send business owner email confirming replacement acceptance

</td><td>

Sends the business owner confirmation that after reviewing the replacement request and coordinating with supplier, the replacement is feasible.

</td></tr><tr><td rowspan="3">

Close case

</td><td>

Notify the requestor

</td><td>

Sends the business owner confirmation that their replacement has been processed successfully.

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

[Process a return request in playbook](playbook-return-request.md)

[Process an edit receipt request in playbook](playbook-process-edit-receipt.md)

[Fulfilling request for copy of contract in playbook](../concept/fulfilling-request-for-contract.md)

[Routing NDAs to suppliers](../concept/routing-ndas-to-suppliers.md)

[Verifying delivery addresses in playbook](../concept/delivery-address-in-playbook.md)

[Reviewing and updating general ledger details in playbook](../concept/general-ledger-details-in-playbook.md)

[Sourcing intake guided experience with playbooks](../concept/sourcing-intake-guided-exp.md)

[Streamlining the supplier risk assessment workflow](../concept/simplify-risk-assessment-wf.md)

