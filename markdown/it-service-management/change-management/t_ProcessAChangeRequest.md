---
title: Process a change request
description: You can approve, implement, review, and close a change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/t\_ProcessAChangeRequest.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use, Change Management, IT Service Management]
---

# Process a change request

You can approve, implement, review, and close a change request.

## Before you begin

Role required: itil, admin, sn\_change\_write, or change\_manager

As part of processing a change request, ensure that you have [detected any change conflicts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_RunManualConflictDetection.md) and [performed risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_AssessRisk.md)

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Select a change request you like to work on.

3.  Approve or reject multiple change requests from the list view.

    To see all the approvals routed to you, navigate to **Self-service** &gt; **My Approvals**. Approvers with the `approval_user` role act only on the approval record.

4.  You can perform the following actions on a change request based on your role.

<table id="choicetable_yhp_ddv_tt"><tbody><tr><td id="d154760e126">

**Approve or reject a change request**

</td><td>

Open the approval record from the **Self-Service** &gt; **My Approvals** module or from the **Approvers** related list on the change request or **Reject** to reject it.The change request changes to the **Scheduled** state if it is approved or to **New** state if it is rejected.

</td></tr><tr><td id="d154760e159">

**Implement a change request**

</td><td>

Select **Implement** to put the change request to the Implement state.**Note:**

When you select **Implement**, the system automatically creates two change tasks:-   **Implement**: Represents the implementation work to be performed.
-   **Post-implementation testing**: Covers testing and validation after implementation.
The system creates theses tasks when the change request enters to **Implement** state. You can modify task assignments, dates and descriptions as needed. To cancel a task, set its state to **Cancelled**.

Tasks remain open until you close or cancel them. Canceling a task does not affect the parent change request.

</td></tr><tr><td id="d154760e203">

**Review a change request**

</td><td>

Select **Review** after reviewing the details on the change request. The change request is moved to the **Review** state. All open change tasks are set to **Canceled**.

</td></tr><tr><td id="d154760e224">

**Close a change request**

</td><td>

Select **Close** after entering the **Close code** and **Close notes** in the **Closure Information** section.The change request is closed.

</td></tr><tr><td id="d154760e248">

**Cancel a change request**

</td><td>

From the context menu, Select **Cancel Change**. Provide a reason for canceling the change and select **Save**.The change request is canceled and the reason for canceling the change is added to the **Work Notes** field.

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


-   **[Associated CIs on a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/c_AffectedCIsAndImpactedServices.md)**  
You can associate additional CIs or services to change requests through related lists on the Change Request form. You can also associate CIs with a change request from the dependency views map.
-   **[Mass Update CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/bulk-ci-change.md)**  
The Mass Update CI plugin enable users to apply the same update to a set of CIs for a specific CI class. The Change Management - Mass Update CI plugin is intended to be used when the Change Management - State Model plugin is activated.
-   **[Use Mass Update CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/use-bulk-mass-ci-changes.md)**  
You can use the proposed changes in a change request to apply the same update to a set of CIs for a specific CI class.
-   **[Place a change request on hold](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_PlaceAChangeRequestOnHold.md)**  
You can put a change request on hold to get additional information for the created change request.
-   **[Refresh impacted services and CIs for Change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/refresh-impacted-services-cis.md)**  
The Impacted services and CIs related list refreshes its records and also the records listed in the Service Offerings and Business Applications related lists based on the affected CIs. You can identify the impacted services and CIs and take necessary action.

**Parent Topic:**[Using Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/using-change-management.md)

**Related topics**  


[Create a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_CreateAChange.md)

