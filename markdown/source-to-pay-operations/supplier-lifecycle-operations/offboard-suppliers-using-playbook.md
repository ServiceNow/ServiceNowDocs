---
title: Offboard suppliers using the supplier offboarding playbook
description: Supplier owners and supplier managers can use the supplier offboarding playbook to complete the tasks and activities that are needed to offboard suppliers.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Offboard a supplier, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Offboard suppliers using the supplier offboarding playbook

Supplier owners and supplier managers can use the supplier offboarding playbook to complete the tasks and activities that are needed to offboard suppliers.

## Offboard a Supplier playbook

The Offboard a Supplier playbook provides step-by-step guidance for completing various stages and activities to offboard a supplier.

When a supplier manager or supplier owner submits the Offboard a supplier case from the Source-to-Pay Workspace, the application opens the case on the Playbook tab on the Details page.

The Offboard a Supplier playbook is displayed only for the cases of type Offboard a supplier.

![Offboard a Supplier playbook tab.](../image/slo-offboard-playbook.png)

## Offboard a Supplier playbook stages and activities

The following table lists the stages and activities that supplier managers and owners can use to offboard suppliers.

<table id="table_onboarding_case_playbook"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

**Review case**

</td><td>

Assign case

</td><td>

When a supplier manager or owner creates an supplier offboarding case, the workspace opens the Create New Onboarding Case form, and then opens the supplier offboarding playbook.

 As a supplier manager or fulfiller, you can use this activity to assign the case to a different person or keep the case assigned to you.

 You can do the following:

 -   In the **Assigned to** search field, search for and select the person that you want to assign the case to.
-   In the **Short description** field, update the description for the case.
-   Select **Save**.

 Select **Start work** to start working on the case.

</td></tr><tr><td>

**Notification Emails**

</td><td>

Review incomplete cases

</td><td>

This activity shows the list of all pending or outstanding cases that you can review before offboarding the supplier.Available actions:

Select **Continue** to move to the next activity.

</td></tr><tr><td>

 

</td><td>

Review incomplete tasks

</td><td>

This activity shows the list of all pending or outstanding tasks that you can review before offboarding the supplier.Select **Continue** to move to the next activity.

</td></tr><tr><td>

 

</td><td>

Notify internal stakeholders

</td><td>

This activity enables you to send an email to notify internal stakeholders about the decision to offboard the supplier.

 A draft email appears with pre-populated data in the **Subject** field. The email body is pre-populated with the relevant text.

 Add the relevant internal stakeholders in the **To** field.

 Select one of the following actions:

 -   **Send Email**: Sends an email to the internal stakeholders.
-   **Skip**: Skips this activity and moves to the next activity.

</td></tr><tr><td>

 

</td><td>

Notify supplier

</td><td>

This activity enables you to send an email to the supplier informing about their termination.A draft email appears with pre-populated data in the **To** and **Subject** fields. The email body is pre-populated with the relevant text.

Select one of the following actions:

-   **Send Email**: Sends an email to the supplier.
-   **Skip**: Skips this activity and moves to the next activity.

</td></tr><tr><td>

**Termination plan**

</td><td>

Decide if a due diligence request is needed

</td><td>

This activity enables you to request for due diligence for the supplier being offboarded. This helps you in assessing the impact of offboarding the supplier.

**Note:** This activity is displayed only if you have installed both the com.snc.sn\_supplier\_tprm and com.sn\_tprm\_onboarding plugins.

 -   Select one of the following options:
    -   **Offboard an engagement with due diligence**: Select this option if you want to create a due diligence request for the supplier.
    -   **Offboard an engagement with NO due diligence**: Select this option if you do not want to create a due diligence request for the supplier.
-   If you selected **Offboard an engagement with due diligence**, then do the following:
    -   In the **Third party** field, enter the name of the supplier.
    -   In the **User who will respond to the initial IRA questionnaire** field, specify the name of the TPRM assessor.
    -   In the **Engagement** field, select the engagement for the supplier.
    -   Select **Submit**.

</td></tr><tr><td>

 

</td><td>

Wait for risk process to start

</td><td>

As soon as the Due Diligence Request moves to the IRQ in progress state, this activity auto-completes and moves to the next activity.

</td></tr><tr><td>

 

</td><td>

Review contract for compliance

</td><td>

This activity lists all the open contracts for the supplier. Ensure that all the terms and clauses are being followed.Select **Continue** to move to the next activity.

</td></tr><tr><td>

 

</td><td>

Settle outstanding invoices

</td><td>

Check all outstanding invoices to confirm that all payments or balances have been settled.Select **Continue** to move to the next activity.

</td></tr><tr><td>

**Final Notices**

</td><td>

Review incomplete cases

</td><td>

This activity shows the list of all pending or outstanding cases that you can review before offboarding the supplier.Available actions:

Select **Continue** to move to the next activity.

</td></tr><tr><td>

 

</td><td>

Review incomplete tasks

</td><td>

This activity shows the list of all pending or outstanding tasks that you can review before offboarding the supplier.Select **Continue** to move to the next activity.

</td></tr><tr><td>

 

</td><td>

Notify internal stakeholders

</td><td>

This activity enables you to send an email to notify internal stakeholders about the decision to offboard the supplier.

 A draft email appears with pre-populated data in the **Subject** field. The email body is pre-populated with the relevant text.

 Add the relevant internal stakeholders in the **To** field.

 Select one of the following actions:

 -   **Send Email**: Sends an email to the internal stakeholders.
-   **Skip**: Skips this activity and moves to the next activity.

</td></tr><tr><td>

 

</td><td>

Notify supplier

</td><td>

This activity enables you to send an email to the supplier informing about their termination.A draft email appears with pre-populated data in the **To** and **Subject** fields. The email body is pre-populated with the relevant text.

Select one of the following actions:

-   **Send Email**: Sends an email to the supplier.
-   **Skip**: Skips this activity and moves to the next activity.

</td></tr><tr><td>

**Close case** Manages the case close activities.

</td><td>

Deactivate user accounts

</td><td>

This activity enables you to raise a ticket to the appropriate teams to deactivate user accounts.Select one of the following actions:

-   **Accept**: Deactivates the supplier user accounts.
-   **Skip**: Skipping this activity deactivates the supplier user accounts and moves to the next activity.

</td></tr><tr><td>

 

</td><td>

Close case

</td><td>

This activity enables you to close the case.Do the following:

-   In the **Close notes** field, enter the details when closing the case.
-   Select **Complete case**.

Updates the case to Closed Completed.

</td></tr><tr><td>

 

</td><td>

Update primary contacts active to false

</td><td>

This activity deactivates all the contacts of the offboarded supplier. That is, the **Active** check box is deselected and the **Locked out** check box is selected for the contacts in the Vendor Contact \[vm\_vdr\_contact\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Offboard a supplier from the Source-to-Pay Workspace](../task/offboard-supplier.md)

**Related topics**  


[Offboard a supplier from the Source-to-Pay Workspace](../task/offboard-supplier.md)

