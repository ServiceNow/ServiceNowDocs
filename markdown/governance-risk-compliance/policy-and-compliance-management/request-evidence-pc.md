---
title: Request evidence during audits
description: Request evidence at any stage during an audit. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Manage evidence requests, Classic UI, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Request evidence during audits

Request evidence at any stage during an audit. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.

## Before you begin

Role required: sn\_audit.user

## About this task

An evidence can be requested in the following three ways:

-   **My Evidence**

    By creating an evidence record from the **My Evidence** module.

-   **Request Evidence**

    From the Entity, Control, Audit Task, Control Test Issue, and Other Issues related lists in an engagement record. To request evidence from these sources, navigate to **Audit** &gt; **Engagements** &gt; **My Engagements**. Open the engagement record, and select the related list from which you want to request evidence. From the **Action on selected rows** list, select **Request Evidence**. Here, you can either create a new evidence request or add more requests to an existing evidence request. The Evidence request is created but not evidence request tasks. For more information on adding existing evidence, see [Reuse existing evidence from the related items of an engagement](request-evidence-existing-pc.md).

-   **Entity, Control, Control Objective, Control Test, Engagement, Issue tables**

    From tables such as Entity, Control, Control Objective, Control Test, Engagement, Issue. However, when the users request evidence from these tables, the evidence request is created not the actual evidence request task. The users must navigate to the evidence request record that is generated and then add evidence request tasks.


In this procedure, the method to request evidence from the **My Evidence** module is described.

## Procedure

1.  Navigate to **Audit** &gt; **My Evidence Request**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Unique number of the evidence request.|
    |Requester|User requesting evidence. This field is automatically populated.|
    |Requested on behalf of|User for whom evidence is being requested.|
    |Assignment group|Group assigned to provide evidence.|
    |Assigned to|User responsible for providing the evidence.|
    |State|State of the request. The default state is **Draft**.|
    |Type|Type of evidence that is created. Can be either Audit or Compliance.|
    |Request reason|Reason for requesting evidence.|
    |Watch list|Users interested in viewing the evidence collected. If a person is added on the watch list, they can navigate to **Audit** &gt; **Evidence Request** &gt; **Watched Evidence Requests** to view the requests.|
    |Name|Name of the evidence request.|
    |Description|Detailed description of the evidence request.|
    |Schedule|
    |Due date|Expected date of evidence submission.|
    |Opened|Date the request is opened. This date is automatically updated.|
    |Closed|Date the request is closed. This date is automatically updated.|
    |Activity|
    |Work notes|Type any notes that might be required.|
    |Activities|Activity log for the request.|

4.  Save the form.

    The Evidence Collection Details related list appears. This related list is used to list the items for which evidence is requested.

5.  Click **New**.

6.  On the form, fill in the fields.

<table id="table_aly_m34_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Evidence request

</td><td>

Unique number of the evidence request task.

</td></tr><tr id="row_evidence_request_policy"><td>

Evidence for

</td><td>

Record for which evidence is requested. Lists all tables to which the evidence is applied.

</td></tr><tr><td>

Name

</td><td>

Evidence collection detail name.

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to provide evidence. The users of this group must have the sn\_grc.business\_user roles.

</td></tr><tr><td>

Assigned to

</td><td>

User responsible for providing evidence.

</td></tr><tr><td>

Evidence collection instructions

</td><td>

Instructions for providing evidence. For example, list of supporting documents, files, and so on.

</td></tr></tbody>
</table>7.  Click **OK**.

8.  Click **Submit**.

9.  Click **Request Evidence**.

    When an evidence request is already in the Work in Progress state, and a new evidence collection detail is added, then evidence request task is sent to the assignee immediately.

    The Evidence related list appears with the list of evidences and the person who is assigned the request receives an email notification to provide the requested evidence. Also, the state of the request changes to **Work in Progress**.

10. Navigate to **Audit** &gt; **Evidence Request** &gt; **My Evidence Request Tasks**.

11. Open the record for which you want to provide evidence.

12. Click **Accept Work**.

13. On the form, fill in the fields.

<table id="table_q2l_wqx_zmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of the evidence request. This value is generated by default.

</td></tr><tr><td>

Requester

</td><td>

User requesting evidence. This value is generated by default.If you are the approver, requester, watch list member, or user in the Assigned to field, then you can edit the details in the **Watch list**, **Name**, and **Description** fields when the evidence is in **New** or **Work in progress** states.

</td></tr><tr><td>

Requested on behalf of

</td><td>

User for whom evidence is being requested. This value is generated by default.

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to provide evidence. The users of this group must have the sn\_grc.business\_user roles.

</td></tr><tr><td>

Assigned to

</td><td>

User responsible for providing the evidence. This value is generated by default.

</td></tr><tr><td>

State

</td><td>

State of the request.

</td></tr><tr><td>

Substate

</td><td>

None. This value is generated by default.

</td></tr><tr><td>

Request reason

</td><td>

Reason for requesting evidence.

</td></tr><tr><td>

Approvers

</td><td>

Users to approve evidence before it is returned to the requester for review. Usually, an approver is the manager of the person providing the evidence.

</td></tr><tr><td>

Watch list

</td><td>

Users interested in viewing the evidence collected.

</td></tr><tr><td>

Name

</td><td>

Name of the evidence request. The name defaults to Evidence collection details name.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the evidence request. The description defaults to the description given in the Evidence request form.

</td></tr><tr><td class="sub-head" colspan="2">

Request Details

</td></tr><tr><td>

Evidence request

</td><td>

Unique ID of the evidence request associated with the task. This value is generated by default and is fetched from the record that was created to request evidence.

</td></tr><tr><td>

Evidence for

</td><td>

Record for which the evidence is requested.

</td></tr><tr><td>

Evidence for description

</td><td>

Description of the record for which the evidence is being requested. This value is generated by default and is fetched from the record that was created to request evidence.

</td></tr><tr><td>

Evidence collection instructions

</td><td>

Instructions to collect the evidence.If you are the manager or requester, you can edit this field when the evidence request task is in work in progress state.

</td></tr></tbody>
</table>14. To request approval for the attached evidence, click **Request Approval**.

15. If no approvers are required, click **Request Review**.

16. Navigate to **Audit** &gt; **Evidence Request** &gt; **My Approvals**.

17. Open the record for which you want to approve evidence.

18. Review the attached evidence on the form and click one of the following options:

    |Option|Description|
    |------|-----------|
    |**Approve**|Approve the attached evidence. The requester gets the evidence provided.|
    |**Request Revision**|Request that the attached evidence be reviewed. Enter comments when you request revision. The assignee gets a notification to review the attached evidence.|
    |**Request Information**|Seek more information and details about the attached evidence. The assignee gets a notification to provide more information about the attached evidence.|

19. Navigate to **Audit** &gt; **Evidence Request** &gt; **My Pending Reviews**.

20. On the Evidence form, review the attached evidence, and click one of the following options:

    |Option|Description|
    |------|-----------|
    |**Accept Evidence**|Accept the evidence that is provided.|
    |**Request Revision**|Request for the evidence to be reviewed, if it is not appropriate, or modified.|
    |**Cancel**|Cancel the evidence request task.|
    |**Delete**|Delete the evidence request task.|

21. Navigate to the form for which you want to display the **Evidence Request** related list.

22. Right-click in the form header, and click **Configure** &gt; **Related Lists**.

23. Locate the **Related Evidence** item in the **Available** box and move it to the **Selected** box.

24. Click **Save**.


