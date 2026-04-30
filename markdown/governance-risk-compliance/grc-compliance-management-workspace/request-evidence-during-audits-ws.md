---
title: Request evidence during audits using the Compliance Workspace
description: Request evidence at any stage during an audit using the Compliance Workspace. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Manage evidence requests using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Request evidence during audits using the Compliance Workspace

Request evidence at any stage during an audit using the Compliance Workspace. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.

## Before you begin

Role required: sn\_audit.user

## About this task

Evidence can be requested in the following three ways:

-   **My Evidence**

    By creating an evidence record from the **My Evidence** module.

-   **Request Evidence**

    From the Entity, Control, Audit Task, Control Test Issue, and Other Issues related lists in an engagement record. To request evidence from these sources, navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**. In the List view of the workspace, select **Engagements** in the Control testing list. Open the engagement record, and select the related list from which you want to request evidence. Select the **Request Evidence** button. Here, you can either create an evidence request or add more requests to an existing evidence request. The Evidence request is created but not the evidence request tasks.

    You can inform the user of the evidence records that already exist for any of the related item tables of the engagement, which they can reuse.

    1.  To create a new evidence request, select **Create a new evidence request** in the **Select method** list of the Request Evidence pop-up. Enter the details and select the **Request** button.
    2.  To view the information about existing related evidences, select the **View** link in the Request Evidence pop-up.

        **Note:** If there is no existing evidence, then the message does not appear in the Request Evidence pop-up.

        ![View link in Request evidence pop-up.](../image/ViewLinkReqEvidencePopup.png "View link in Request evidence pop-up")

    3.  To view all existing evidences created on the related items, select the Evidence related list.

        When the evidence is in **Closed Complete** state, the UI action buttons such as **New**, **Add existing evidence**, **Remove**, and **Delete** are disabled. You can perform these UI actions only when the engagement or any other audit and compliance object is in an active state.

    4.  To add existing evidence, select the **Add Existing Evidence** button and select the evidence.

        **Note:** The **Add Existing Evidence** button is available in the Evidence related item of all compliance and audit objects in the Compliance Workspace such as Engagement, Audit task, Issue, Policy, Entity, Control, Control Objective, Authority document, Citations, and Evidence request.

    5.  To remove the association of the evidences linked to the engagement, select the evidences in the Evidence related list and select the **Remove** button.

        **Note:** The action only removes the association of the existing evidence records from the engagement and doesn’t remove the evidence record from the database.

    **Note:** The logged-in user must also have access to the engagement for which evidence records exist or must be the user who has access to the record to view and add them. If the logged-in user doesn’t have access to those records, although there are evidenced existing on those related items, they aren’t displayed for the user to add.

-   **Entity, Control, Control Objective, Control Test, Engagement, Issue tables**

    From tables such as Entity, Control, Control Objective, Control Test, Engagement, Issue. However, when the users request evidence from these tables, the evidence request is created not the actual evidence request task. The users must navigate to the evidence request record that is generated and then add evidence request tasks.


In this procedure, the method to request evidence from the **My Evidence** module is described.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Evidence requests** &gt; **My request**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_afd_4gk_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the evidence request.

</td></tr><tr><td>

Name

</td><td>

A name for this request.

</td></tr><tr><td>

Requester

</td><td>

User requesting evidence. This field is automatically populated.

</td></tr><tr><td>

Requested on behalf of

</td><td>

User for whom evidence is being requested.

</td></tr><tr><td>

Type

</td><td>

Type of evidence that is created. Can be either Audit or Compliance.

</td></tr><tr><td>

Request reason

</td><td>

Reason for requesting evidence.

</td></tr><tr><td>

State

</td><td>

State of the request. The default state is **Draft**.

</td></tr><tr><td>

Substate

</td><td>

An additional state for the request.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the evidence request.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to provide evidence.

</td></tr><tr><td>

Assigned to

</td><td>

User responsible for providing the evidence.

</td></tr><tr><td>

Watch list

</td><td>

Users interested in viewing the evidence collected. If a person is added on the watch list, they can navigate to **Audit** &gt; **Evidence Request** &gt; **Watched Evidence Requests** to view the requests.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

Expected date of evidence submission.

</td></tr><tr><td>

Opened

</td><td>

Date the request is opened. This date is automatically updated.

</td></tr><tr><td>

Closed

</td><td>

Date the request is closed. This date is automatically updated.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes

</td><td>

Type any notes that might be required.

</td></tr><tr><td>

Activities

</td><td>

Activity log for the request.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.For more information on the confidential option, see [Confidentiality flag for audit and compliance records](../../grc-audit/concept/confidentiality-flag-audit-pc.md).

</td></tr></tbody>
</table>6.  Save the form.

    Monitor the state of the Evidence in the stepper of the Overview page. The record progresses through a sequence of logical steps when you accept evidence, request revision of the evidence, and request information.

    The Evidence collection details related list appears. This related list is used to list the items for which evidence is requested.

7.  Select **New**.

8.  On the form, fill in the fields.

<table id="table_aly_m34_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the evidence collection detail.

</td></tr><tr><td>

Name

</td><td>

A name for this request.

</td></tr><tr id="row_evidence_request_policy"><td>

Evidence collection type

</td><td>

Record for which evidence is requested. If the request was entered by a user with the compliance user role, the available options are:

-   Authority document
-   Citation
-   Control
-   Control objective
-   Control test
-   Entity
-   Issue
-   Policy
 If the request was entered by a user with the audit user role, the available options are:

-   Audit task
-   Control
-   Control objective
-   Control test
-   Engagement
-   Entity
-   Issues


</td></tr><tr><td>

Evidence for

</td><td>

Lists all the tables to which the evidence is applied.

</td></tr><tr><td>

Evidence request

</td><td>

Unique number of the evidence request task.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to provide evidence. The users of this group must have the sn\_grc.business\_user roles.

</td></tr><tr><td>

Assigned to

</td><td>

User responsible for providing evidence.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Instructions

</td></tr><tr><td>

Evidence collection instructions

</td><td>

Instructions for providing evidence. For example, list of supporting documents, files, and so on.

</td></tr></tbody>
</table>9.  Select **Save**.

10. Select **Request Evidence**.

    When an evidence request is already in the Work in Progress state, and a new evidence collection detail is added, the evidence request task is sent to the assignee immediately.

    The Evidence related list appears with the list of evidences and the person who is assigned the request receives an email notification to provide the requested evidence. Also, the state of the request changes to **Work in Progress**.You can view the description and monitor the state of the Evidence request in the stepper of the Overview page as it progresses through the evidence request process flow.


