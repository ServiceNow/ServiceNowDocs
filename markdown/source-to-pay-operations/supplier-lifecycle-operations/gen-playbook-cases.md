---
title: Case playbook for specific supplier case types
description: Source-to-Pay Workspace includes a generic case playbook to complete supplier cases of specific case types.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Case playbook for specific supplier case types

Source-to-Pay Workspace includes a generic case playbook to complete supplier cases of specific case types.

## Case playbook for supplier cases

The case playbook provides step-by-step guidance for completing specific types of supplier cases. The case playbook includes a generic supplier case flow containing various stages and activities that you must complete to close the supplier case. For more information, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

When a supplier contact submits a request using the supplier catalog item from the Supplier Collaboration Portal or when a supplier manager or fulfiller creates a case from the Source-to-Pay Workspace, the application opens the case on the **Playbook** tab on the Details page.

The case playbook is displayed only for these case types:

-   Supplier issue
-   Supplier support request
-   General inquiry

## Case playbook flow

The following diagram illustrates the flow of the activities in each stage of the Case playbook.

## Case playbook stages and activities

The case playbook contains the following stages and activities.

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

As a supplier manager or fulfiller, you can use this activity to assign the case to a different person or keep the case assigned to you.You can do the following:

 -   In the **Assigned to** search field, search for and select the person that you want to assign the case to.
-   In the **Short description** field, update the description for the case.
-   Select one of the following actions:
    -   Select **Save** to save your changes.
    -   Select **Start work** to start working on the case.

</td></tr><tr><td rowspan="3">

Close the case record

</td><td>

Notify the supplier

</td><td>

A draft email appears with pre-populated data in the **To** and **Subject** fields. The email body is pre-populated with the relevant text.

 Select one of the following actions:

 -   **Send Email**: Send an email to the supplier informing that the request has been completed.
-   **Skip**: Skips this activity and moves to the next activity.

</td></tr><tr><td>

Escalate task priority

</td><td>

The supplier manager or fulfiller can use this option only for supplier document related cases, when the following conditions are met:-   case is of the type supplier issue
-   case has a related task and the task action is of the type Upload document
-   task state is Awaiting Completion.
-   a document reference is provided

To escalate the task priority, the supplier manager or fulfiller can select a higher task priority from the Priority dropdown.

</td></tr><tr><td>

Complete case

</td><td>

As a supplier manager or fulfiller, you can update the state of the case and close the case.

 You can do the following:

 -   From the State drop-down list, select **Closed completed**.
-   In the **Work notes** field, provide any additional information about the case.
-   In the **Close notes** field, enter the details when closing the case.
-   Select **Complete case**.

</td></tr></tbody>
</table>**Parent Topic:**[Manage supplier cases from the Source-to-Pay Workspace](managing-cases.md)

**Related topics**  


[Manage supplier cases from the Source-to-Pay Workspace](managing-cases.md)

[Configure due dates for supplier cases](../task/configure-case-due-date.md)

[Playbook for updating the supplier primary data](primary-playbook-cases.md)

[Create a case on behalf of a supplier from the Source-to-Pay Workspace](../task/create-new-supplier-case.md)

