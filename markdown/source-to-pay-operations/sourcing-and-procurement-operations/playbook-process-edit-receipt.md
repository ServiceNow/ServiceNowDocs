---
title: Process an edit receipt request in playbook
description: You can revise previously approved receipts to correct any discrepancies, ensuring the delivery receipt accurately reflects the quantities received for a specific purchase order.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Process an edit receipt request in playbook

You can revise previously approved receipts to correct any discrepancies, ensuring the delivery receipt accurately reflects the quantities received for a specific purchase order.

## Before you begin

Role required: Fulfiller, agent, or admin

## About this task

As a fulfiller, you can review the details of the Edit Receipt request and choose to either confirm or reject it.

**Note:** This task is not required if the `sn_spend_cp.enable_automated_edit_receipt_flow` system property is enabled. For more information, see [Components installed with Sourcing and Procurement Operations](../reference/installed-with-FSC.md).

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select **All work** &gt; **Cases**.

3.  Select the case of type Edit a receipt.

    ![Procurement case of type Edit a receipt.](../image/edit-receipt-s2pws.png)

4.  Complete the steps in the various stages and activities of the Edit a receipt playbook.

    ![Playbook receipt](../image/edit-receipt-playbook.png)

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
-   In the **Case type:** field, leave the default value as-is.
-   In the **Short description** field, add a brief description for the case.
-   In the **Description** field, add a detailed description for the case.
-   Select one of the following actions:
    -   Select **Save** to save your changes.
    -   Select **Start work** to start working on the case.


</td></tr><tr><td>

Intake and Assess

</td><td>

Modifications requested by shopper

</td><td>

Review the changes requested by the shopper on the delivery receipt.

</td></tr><tr><td rowspan="3">

Review and confirm

</td><td>

Confirm edit

</td><td>

Review this request to edit the delivery receipt and confirm or reject whether it can be processed.Select one of the following actions.

-   **Confirm**: When you confirm, the procurement case moves to Work in progress state.
-   **Reject**: When you reject, the procurement case moves to Closed Rejected state.


</td></tr><tr><td>

Edit delivery receipt

</td><td>

Updates the delivery receipt with the changes requested by the shopper

</td></tr><tr><td>

Update purchase order line

</td><td>

Updates the purchase order line with the quantity of items received, as specified by the shopper.

</td></tr><tr><td rowspan="2">

Close case

</td><td>

Notify the requester

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

</td></tr></tbody>
</table>
**Parent Topic:**[Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace](../concept/work-playbooks-spo.md)

**Related topics**  


[Process a purchase order edit in playbook](process-purchase-order.md)

[Process a purchase requisition edit request in playbook](playbook-edit-request-flow.md)

[Process a return request in playbook](playbook-return-request.md)

[Process a replacement request in playbook](playbook-replacement-request.md)

[Fulfilling request for copy of contract in playbook](../concept/fulfilling-request-for-contract.md)

[Routing NDAs to suppliers](../concept/routing-ndas-to-suppliers.md)

[Verifying delivery addresses in playbook](../concept/delivery-address-in-playbook.md)

[Reviewing and updating general ledger details in playbook](../concept/general-ledger-details-in-playbook.md)

[Sourcing intake guided experience with playbooks](../concept/sourcing-intake-guided-exp.md)

[Streamlining the supplier risk assessment workflow](../concept/simplify-risk-assessment-wf.md)

