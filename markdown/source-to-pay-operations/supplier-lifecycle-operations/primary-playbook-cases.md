---
title: Playbook for updating the supplier primary data
description: Source-to-Pay Workspace includes a playbook that you use for updating the supplier primary data.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage supplier details, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Playbook for updating the supplier primary data

Source-to-Pay Workspace includes a playbook that you use for updating the supplier primary data.

## Review supplier primary data request playbook

This playbook provides step-by-step guidance for cases related to updating supplier primary data. The playbook includes a supplier case flow containing various stages and activities that you must complete to close the supplier case. For more information, see Interact with Playbook.

This playbook is used for updating the supplier primary data when:

-   A supplier contact submits a request for updating the supplier primary data using the supplier catalog item from the Supplier Collaboration Portal
-   A supplier manager or fulfiller creates a case for updating the supplier primary data from the Source-to-Pay Workspace

The application opens the case on the **Playbook** tab on the Details page.

This playbook is displayed only for these case types:

-   Banking information change request
-   Supplier information change request
-   Supplier location change request
-   Conduct sanction screening

![Review supplier primary data request playbook.](../image/primary-data-playbook.png "Review supplier primary data request playbook on the Playbook tab")

## Review supplier primary data request playbook flow

The following diagram illustrates the flow of the activities in each stage of the Review supplier primary data request playbook.

![Review supplier primary data request playbook.](../image/primary-data-playbook-flow.png "Review supplier primary data request playbook flow")

## Review supplier primary data request playbook stages and activities

The playbook contains the following stages and activities.

<table id="table_bgd_tzx_ztb"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td rowspan="2">

Review case

</td><td>

Assign case

</td><td>

As a supplier manager or fulfiller, you can use this activity to assign the case to a different person or keep the case assigned to you.You can do the following:

 -   In the **Assigned to** search field, search for and select the person that you want to assign the case to.
-   In the **Short description** field, update the description for the case.
-   Select one of the following actions:
    -   Select **Save** to save your changes.
    -   Select **Start work** to start working on the case.

</td></tr><tr><td>

Approve changes

</td><td>

As a supplier manager or fulfiller, you can use this activity to decide whether to approve or reject the case.

 This activity has the options:

-   Approve changes: Approves your changes.
-   Reject changes: Rejects your changes and opens the Reject changes stage.

 For more information, see Non-Interactive activities.

</td></tr><tr><td rowspan="3">

Process change request

</td><td>

Verify changes are made in other systems

</td><td>

This activity informs you that changes to this request have been processed in ServiceNow. If applicable, please verify that the details of this case have also been processed in all other systems.You can do the following:

 -   **Skip**: Skips this activity and moves to the next activity.
-   **Continue**: Marks this activity as complete and moves to the next activity.

</td></tr><tr><td>

Notify the supplier

</td><td>

A draft email appears with pre-populated data in the **To** and **Subject** fields. The email body is pre-populated with the relevant text.

 You can do the following:

 -   **Send Email**: Send an email to the supplier informing that the request has been completed.
-   **Skip**: Skips this activity and moves to the next activity.

</td></tr><tr><td>

Complete case

</td><td>

As a supplier manager or fulfiller, you can update the state of the case and complete the case.

You can do the following:

-   From the State drop-down list, select **Closed completed**.
-   In the **Work notes** field, provide any additional information about the case.
-   In the **Close notes** field, enter the details when closing the case.
-   Select **Complete case**.

Updates the case to Closed Completed.

</td></tr><tr><td rowspan="2">

Reject Changes

</td><td>

Notify the supplier

</td><td>

A draft email appears with pre-populated data in the **To** and **Subject** fields. The email body is pre-populated with the relevant text.

 You can do the following:

 -   **Send Email**: Send an email to the supplier informing that the request has been rejected.
-   **Skip**: Skips this activity and moves to the next activity.

</td></tr><tr><td>

Complete case

</td><td>

As a supplier manager or fulfiller, you can update the state of the case and reject the case.

You can do the following:

-   From the State drop-down list, select **Closed rejected**.
-   In the **Work notes** field, provide any additional information about the case.
-   In the **Close notes** field, enter the details when closing the case.
-   Select **Complete case**.

Updates the case to Closed Rejected.

</td></tr></tbody>
</table>**Parent Topic:**[Manage supplier details](supp-ws-details-page.md)

**Related topics**  


[Manage supplier cases from the Source-to-Pay Workspace](managing-cases.md)

[Configure due dates for supplier cases](../task/configure-case-due-date.md)

[Case playbook for specific supplier case types](gen-playbook-cases.md)

[Create a case on behalf of a supplier from the Source-to-Pay Workspace](../task/create-new-supplier-case.md)

