---
title: Process a change request
description: You can approve, implement, review, and close a change request.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Change Management, IT Service Management]
---

# Process a change request

You can approve, implement, review, and close a change request.

## Before you begin

Role required: itil, admin, sn\_change\_write, or change\_manager

As part of processing a change request, ensure that you have [detected any change conflicts](t_RunManualConflictDetection.md#) and [performed risk assessment](t_AssessRisk.md)

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Select a change request you like to work upon.

3.  You can perform the following actions on a change request based on your role.

<table id="choicetable_yhp_ddv_tt"><tbody><tr><td id="d145296e105">

**Approve or reject a change request**

</td><td>

Open the approval record and click **Approve** to approve the change request or **Reject** to reject it.The change request changes to the **Scheduled** state if it is approved or to **New** state if it is rejected.

</td></tr><tr><td id="d145296e129">

**Implement a change request**

</td><td>

Click **Implement** to put the change request into action.The change request state changes to **Implement**. The workflow creates two change tasks: **Implement** and **Post-implementation testing**. Review the change tasks and assign them to a user or group, as appropriate.

</td></tr><tr><td id="d145296e153">

**Review a change request**

</td><td>

Click **Review** after reviewing the details on the change request. The change request is moved to the **Review** state. All open change tasks are set to **Canceled**.

</td></tr><tr><td id="d145296e174">

**Close a change request**

</td><td>

Click **Close** after entering the **Close code** and **Close notes** in the **Closure Information** section.The change request is closed.

</td></tr><tr><td id="d145296e198">

**Cancel a change request**

</td><td>

From the context menu, click **Cancel Change**. Provide a reason for canceling the change and click **Save**.The change request is canceled and the reason for canceling the change is added to the **Work Notes** field.

</td></tr></tbody>
</table>    **Note:** Manually created change tasks are not automatically closed or cancelled when state is changed from Implement to Review. You must first close the change tasks and to close the change request.

    Users with approval\_user role, who approve change requests, do not have access to the change request itself. The following information are made available within the approval record to help these users make the right approval decision:

    -   Number
    -   Requested by
    -   Configuration Item
    -   Type
    -   Planned Start Date
    -   Risk
    -   Planned End Date
    -   Impact
    -   Short Description
    -   Description
    -   Justification
    -   Implementation plan
    -   Risk and impact analysis
    -   Backout plan
    You can also add approval history to the change request activity log. Click the activity filter icon and select **Approval history** from the list. When there is a change in the approval process, such as an approval, rejection, or comments, the activity log is updated.


-   **[Associated CIs on a change request](../concept/c_AffectedCIsAndImpactedServices.md#)**  
You can associate additional CIs or services to change requests through related lists on the Change Request form. You can also associate CIs with a change request from the dependency views map.
-   **[Mass Update CI](../concept/bulk-ci-change.md)**  
The Mass Update CI plugin enable users to apply the same update to a set of CIs for a specific CI class. The Change Management - Mass Update CI plugin is intended to be used when the Change Management - State Model plugin is activated.
-   **[Use Mass Update CI](use-bulk-mass-ci-changes.md)**  
You can use the proposed changes in a change request to apply the same update to a set of CIs for a specific CI class.
-   **[Place a change request on hold](t_PlaceAChangeRequestOnHold.md)**  
You can put a change request on hold to get additional information for the created change request.
-   **[Refresh impacted services and CIs for Change](refresh-impacted-services-cis.md)**  
The Impacted services and CIs related list refreshes its records and also the records listed in the Service Offerings and Business Applications related lists based on the affected CIs. You can identify the impacted services and CIs and take necessary action.

**Parent Topic:**[Using Change Management](../concept/using-change-management.md)

**Related topics**  


[Create a change request](t_CreateAChange.md)

