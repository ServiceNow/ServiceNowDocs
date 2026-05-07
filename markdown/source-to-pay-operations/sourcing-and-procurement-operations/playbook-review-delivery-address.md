---
title: Review delivery address in playbook
description: Verify a delivery address presented through the playbook by evaluating the address against supplier addresses and indicating whether it’s valid.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Verifying delivery addresses in playbook, Working with playbooks, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Review delivery address in playbook

Verify a delivery address presented through the playbook by evaluating the address against supplier addresses and indicating whether it’s valid.

## Before you begin

Role required: Fulfiller, agent

![Review delivery address in playbook](../image/pb-delivery-add-ver.png)

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select **All work** &gt; **Cases**.

3.  Open a procurement case with filter criteria set to **Delivery Address Review** and the **State** set to In review.

4.  Complete the steps in the various stages and activities of the Verify and approve delivery address playbook.

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


</td></tr><tr><td>

Verify and approve address

</td><td>

Check that the address is verified and company approved

</td><td>

This activity enables you to review the delivery address and indicate if it is verified and company approved.The options are:

-   **Not verified**:Select this option if the address provided by the shopper is invalid and can’t be verified.
-   **Verified but not approved**: Select this option if the address provided by the shopper is valid but isn't approved by the supplier company.
-   **Verified and approved**: Select this option if the address provided by the shopper is valid and approved by the supplier company.


</td></tr><tr><td rowspan="2">

Close case

</td><td>

Notify the requestor

</td><td>

Use this activity to email the requestor about the status of the delivery address verification and approval.

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

The procurement case is updated with valid address and its state updates to Closed Completed.

**Parent Topic:**[Verifying delivery addresses in playbook](../concept/delivery-address-in-playbook.md)

