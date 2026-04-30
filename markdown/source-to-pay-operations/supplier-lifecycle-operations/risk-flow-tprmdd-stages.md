---
title: Playbook stages and activities when Third-party Risk Due Diligence is installed
description: The following table lists the Perform risk assessment playbook stages and activities when Third-party risk Due Diligence is installed.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Risk assessment flow with Third-party Risk Due Diligence, Use the risk assessment playbook, Create a supplier, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Playbook stages and activities when Third-party Risk Due Diligence is installed

The following table lists the Perform risk assessment playbook stages and activities when Third-party risk Due Diligence is installed.

<table><thead><tr><th>

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

Update case to work in progress

</td><td>

Updates the state of the due diligence case to work in progress.

</td></tr><tr><td rowspan="4">

Create request

</td><td>

Check if TPRM is installed

</td><td>

Checks if the TPRM plugin is installed.

</td></tr><tr><td>

Check for duplicate due diligence \(risk assessment\) requests

</td><td>

Reviews existing due diligence requests for this supplier.You can do the following:

-   **Cancel:** If there's an existing due diligence request, you can select this option to cancel this due diligence case.
-   **Create new request:** Creates a new due diligence request.

</td></tr><tr><td>

Create due diligence request

</td><td>

Do the following:-   Under Options, select **Onboard a new engagement**.
-   In the **Third party** field, select the supplier.
-   Fill in the required fields in the following sections:
    -   Third-party information
    -   Third-party address
    -   Engagement information
    -   Engagement address
    -   Engagement primary contact
-   Select **Submit**.

</td></tr><tr><td>

Check the status of the due diligence request

</td><td>

Waits for initial approval on the due diligence request and the risk process to start. Select **View record** to view the due diligence request.

</td></tr><tr><td rowspan="3">

Assess risk

</td><td>

Waiting on IRQs to be completed

</td><td>

Waits for the approval of the IRQs and the due diligence to start.

</td></tr><tr><td>

Waiting on the due diligence to be completed

</td><td>

Waits for the due diligence to be completed and the formal review process to start.

</td></tr><tr><td>

Waiting on the due diligence to be reviewed and approved

</td><td>

Waits for the due diligence request to be reviewed and approved.

</td></tr><tr><td>

Review risk rating

</td><td>

Accept or reject risk ratings

</td><td>

Review the risk rating of the supplier and choose to accept or reject the risk rating.Available actions:

-   **Accept**
-   **Reject**

If you select **Reject**, the playbook opens the [Rejection stage](use-playbooks-onboard-supp.md#).


</td></tr><tr><td rowspan="2">

Close case

</td><td>

Notify the requester that the request has been approve

</td><td>

Available actions:-   **Send email:** Sends an email to the requester, informing them that the case has been approved.
-   **Skip:** Skips this activity.

</td></tr><tr><td>

Close case

</td><td>

Add closing comments to complete the case.In the **Close notes** field, add your comments and select **Close case**.

The state of the due diligence case is updated to Closed completed.

</td></tr></tbody>
</table>**Parent Topic:**[Risk assessment flow when Third-party Risk Due Diligence is installed](risk-flow-slo-tprm.md)

**Related topics**  


[Risk assessment flow when Third-party Risk Due Diligence is installed](risk-flow-slo-tprm.md)

