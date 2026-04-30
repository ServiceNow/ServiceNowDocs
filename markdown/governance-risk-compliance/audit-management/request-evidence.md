---
title: Request evidence for audit
description: Request evidence at any stage during an audit. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Evidence request workflow, Audit Evidence Request, Use, Audit Management, Governance, Risk, and Compliance]
---

# Request evidence for audit

Request evidence at any stage during an audit. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.

## Before you begin

Role required: The role required for Audit Management is sn\_audit.user.

Following are the roles required for Lite Audit:

-   sn\_grc\_advanced.evidence\_reader
-   sn\_grc\_advanced.evidence\_requester
-   sn\_grc\_advanced.evidence\_responder
-   sn\_grc\_advanced.evidence\_admin

## About this task

An evidence can be requested in the following three ways:

-   By creating an evidence record from the **My Evidence** module.
-   From the Entity, Control, Audit Task, Control Test Issue, and Other Issues related lists in an engagement record. To request evidence from these sources, navigate to **Audit** &gt; **Engagements** &gt; **My Engagements**. Open the engagement record, and select the related list from which you want to request evidence. From the **Action on selected rows** list, select **Request Evidence**. Here, you can either create a new evidence request or add more requests to an existing evidence request. The Evidence request is created but not evidence request tasks.

    Select **Create a new evidence request task** in the **Request evidence** page to create request task.![New evidence form.](../../grc-workspace-audit/image/request_evidence_itam.png)

-   From the following tables: Entity, Control, Control Objective, Control Test, Engagement, Issue. However, when the users request evidence from these tables, the evidence request is created not the actual evidence request task. The users must go to the evidence request record that is generated and then add evidence request tasks.

In this procedure, the method to request evidence from the **My Evidence** module is described.

## Procedure

1.  Navigate to **Audit** &gt; **My Evidence Request**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_afd_4gk_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the evidence request.

</td></tr><tr><td>

Requester

</td><td>

User requesting evidence. This field is automatically populated.

</td></tr><tr><td>

Requested on behalf of

</td><td>

User for whom evidence is being requested.

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to provide evidence.

</td></tr><tr><td>

Assigned to

</td><td>

User responsible for providing the evidence.

</td></tr><tr><td>

State

</td><td>

State of the request. The default state is **Draft**.

</td></tr><tr><td>

Type

</td><td>

The default type is **Audit**.

</td></tr><tr><td>

Request reason

</td><td>

Reason for requesting evidence.

</td></tr><tr><td>

Watch list

</td><td>

Users interested in viewing the evidence collected. If a person is added on the watch list, they can navigate to **Audit** &gt; **Evidence Request** &gt; **Watched Evidence Requests** to view the requests.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the evidence request.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the evidence request.

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

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.For more information on confidential option, see [Confidentiality flag for audit and compliance records](../concept/confidentiality-flag-audit-pc.md).

</td></tr><tr><td>

Context

</td><td>

The table for the context record.

</td></tr><tr><td>

Context record

</td><td>

Context record for the evidence request.

</td></tr><tr><td>

Source

</td><td>

The object from where the evidence is initiated. Add this to the above table.

</td></tr></tbody>
</table>4.  Save the form.

    The Evidence Collection Details related list appears. This related list is used to list the items for which evidence is requested.

5.  Click **New**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Evidence request|Unique number of the evidence request task.|
    |Evidence for|Record for which evidence is requested.|
    |Assignment group|Group assigned to provide evidence. The users of this group must have the sn\_grc.business\_user roles.|
    |Assigned to|User responsible for providing evidence.|
    |Evidence collection instructions|Instructions for providing evidence. For example, list of supporting documents, files, and so on.|

7.  Click **OK**.

8.  Click **Submit**.

9.  Click **Request Evidence**.

    When an evidence request is already in the Work in Progress state, and a new evidence collection detail is added, then evidence request task is sent to the assignee immediately.

    The Evidence related list appears with the list of evidences and the person who is assigned the request receives an email notification to provide the requested evidence. Also, the state of the request changes to **Work in Progress**.


