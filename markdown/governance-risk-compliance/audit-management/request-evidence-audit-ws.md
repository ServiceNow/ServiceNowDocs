---
title: Request evidence during audits using Audit Workspace
description: Request evidence at any stage during an audit using the Audit Workspace. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Audit Workspace for the Audit supervisor, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Request evidence during audits using Audit Workspace

Request evidence at any stage during an audit using the Audit Workspace. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.

## Before you begin

Role required: sn\_audit.user

## Procedure

1.  Navigate to **All** &gt; **Audit Workspace**.

2.  In the Audit Workspace select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Evidence requests** &gt; **My request**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_f11_nrs_2yb"><thead><tr><th>

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

7.  Click **New**.

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

Record for which evidence is requested. If you’re a user with the audit user role, the available options are:

-   Audit task
-   Authority document
-   Citation
-   Control
-   Control objective
-   Control test
-   Engagement
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

    The Evidence related list appears with the list of evidences and the person who is assigned the request receives an email notification to provide the requested evidence. Also, the state of the request changes to **Work in Progress**.You can view the description. Monitor the state of the Evidence request in the stepper of the Overview page as it progresses through the evidence request process flow.


