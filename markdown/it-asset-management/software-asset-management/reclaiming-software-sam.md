---
title: Reclaim software
description: Optimize your environment by reclaiming or removing installed software that is not being used or used infrequently.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Reclaim software

Optimize your environment by reclaiming or removing installed software that is not being used or used infrequently.

## Before you begin

Role required: sam\_admin

## About this task

Reclaiming software involves a workflow to remove software for a user. You can reclaim software for multiple reasons such as low usage, optimization generated due to consolidation, or overlapping subscriptions. The reclamation process can be managed manually through the creation of tasks or automatically using the Client Software Distribution \(CSD 2.0\) capabilities.

You can select **Show Workflow** at any point of time in the reclamation workflow to see the current stage the workflow is in. For information on CSD 2.0, see [Client Software Distribution 2.0 application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/csd-app-2.md).

Starting from the Australia release, the reclamation workflow can also be completed using the Software Reclamation Flow in the Flow Designer application along with additional error handling functionality.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

2.  Select **License usage**.

3.  Select the **Removal candidates** tab.

4.  Select to open a removal candidate record.

    Ensure that the **Assigned to** field has a value. If not, select a value. Typically, the sam admin role takes ownership of the workflow and ensures that a group is mentioned in the **Assignment group** field. Having a group specified in the **Assignment group** field ensures that the approval goes to the correct group. The assignment group consists of users who can approve or reject a request to keep the software.

5.  Select **Reclaim**

    The state of the removal candidate record changes from **Ready** to **Awaiting User**. An email notification is sent to the user to whom the software license is assigned. The user details are mentioned under the removal candidate section.

    An email notification is sent if the **Notify user** check box is selected in the reclamation rule record. If you don't select the **Notify user** check box, the task and email isn't sent to the user.

    If the user is an ITIL user, then both email and the approval task will be created for the user. However, if the user is not an ITIL user then only an email is sent to the user.

    The email mentions that the software is going to be reclaimed since it's not being used and provides the user with following two options:

    -   **Yes**: indicates keeping the software.
    -   **No**: indicates removing the software.
6.  Select **Yes** or **No**.

    If the user selects **Yes**, the following steps take place:

    1.  A task gets created for the removal candidate record.
    2.  The state of the removal candidate record changes to **Awaiting Approval** as a member of the assignment group needs to approve the request for keeping the software.
    3.  A member of the assignment group approves or rejects the request.
        -   If approved, the request in the email, the removal candidate record automatically moves to the **Close Skipped** state.
        -   If the request is rejected, then the state of the removal candidate record changes to **Awaiting Revocation** which is handled by the sam admin role.

            **Note:**

            In case CSD 2.0 is not installed then the sam admin can assign the request to an individual who can manually uninstall the software. If CSD 2.0 is installed then the software is automatically removed. For more details, refer to the CSD 2.0 documentation.

            If you have optimizations generated for Microsoft 365 products for low usage, consolidate, or overlapping subscription then you can automatically remove the subscriptions from the Microsoft 365 portal.

            If you have integrations or API support reclamations, users will be removed automatically from the portal.

        -   If the installations or subscriptions are manually removed, then the sam admin role must manually mark the workflow as **Close Complete**. However if the process happens automatically then the system automatically updates the workflow record as **Close Complete**.
    If the user selects **No**, the following steps take place:

    1.  The state of the removal candidate record changes to **Awaiting Revocation**.
    2.  Based on the scenarios mentioned in the above note, software removal takes place.

        **Note:** For removal candidates that are grouped into low usage or overlapping justifications, you do not need to manually remove subscriptions as auto reclamation is performed for these two justifications. Fore more information on justifications, see [Software installation optimization and removal](../concept/c_SAMOptimization.md).


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

