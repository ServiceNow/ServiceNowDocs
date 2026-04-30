---
title: Review and update missing general ledger details in playbook
description: Review and update missing General Ledger \(GL\) accounting details through the procurement playbook. If a shopper checks out multiple products from a single supplier, multiple Purchase Requisition Lines \(PRLs\) are generated, some of which could potentially contain missing GL accounting details.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reviewing and updating general ledger details in playbook, Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Review and update missing general ledger details in playbook

Review and update missing General Ledger \(GL\) accounting details through the procurement playbook. If a shopper checks out multiple products from a single supplier, multiple Purchase Requisition Lines \(PRLs\) are generated, some of which could potentially contain missing GL accounting details.

## Before you begin

Role required: Fulfiller, agent

![Review and update missing general ledger details in playbook](../image/pb-gl-review.png)

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select

3.  **All work** &gt; **Cases**.

4.  Open a procurement case with filter criteria set to **GL Coding Review** and the **State** set to In review.

5.  Complete the steps in the various stages and activities of the Verify and approve accounting fields on PRL playbook.

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

**Note:** Ensure that the user to whom the GL Coding review case is assigned is part of the General Ledger Accounting group.

-   In the **Short description** field, update the description for the case.
-   Select one of the following actions:
    -   Select **Save** to save your changes.
    -   Select **Start work** to start working on the case.


</td></tr><tr><td>

Verify and approve accounting fields on PRL

</td><td>

Review PRLs with missing GL account informaiton

</td><td>

This activity enables you to review and update the PRLs.Select a PRL, review the missing GL accounting details, update them, and then select **Save**. Some examples of possible missing information include Capex, expense and pre-payment accounts.

The PRL is updated with GL accounting details.

The options are:

-   **Continue**: Select this option to move to the next stage and activity.
-   **Open List**: Select this option to view a list of PRLs.


</td></tr><tr><td rowspan="2">

Close case

</td><td>

Notify the requestor

</td><td>

Use this activity to email the requestor that the accounting fields on PRL have been verified and approved.

 A draft email appears with pre-populated data in the **Subject** field. The email body is pre-populated with the relevant text.

 Select one of the following actions:

 -   **Send Email**: Sends the email instantly.
-   **Skip**: Skips this activity and moves to the next activity.


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
## Result

The procurement case is updated with valid GL account details and the playbook is closed.

**Parent Topic:**[Reviewing and updating general ledger details in playbook](../concept/general-ledger-details-in-playbook.md)

