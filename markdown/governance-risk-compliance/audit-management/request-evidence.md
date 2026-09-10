---
title: Request evidence for audit using two-step process
description: Request evidence at any stage during an audit. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/audit-management/request-evidence.html
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 6
breadcrumb: [Evidence request workflow, Audit evidence request, Audit Management overview, Audit Management, Governance, Risk, and Compliance]
---

# Request evidence for audit using two-step process

Request evidence at any stage during an audit. The details about the items for which evidence is requested are also provided to the person responsible for providing the evidence.

## Before you begin

Role required: The role required for Audit Management is sn\_audit.user.

Following are the roles required for Lite Audit:

-   sn\_grc\_advanced.evidence\_reader
-   sn\_grc\_advanced.evidence\_requester
-   sn\_grc\_advanced.evidence\_responder
-   sn\_grc\_advanced.evidence\_admin

## About this task

Evidence can be requested in the following three ways:

-   By creating an evidence record from the **My Evidence** module.
-   From the Entity, Control, Audit Task, Control Test Issue, and Other Issues related lists in an engagement record. To request evidence from these sources, navigate to **Audit** &gt; **Engagements** &gt; **My Engagements**. Open the engagement record, and select the related list from which you want to request evidence. From the **Action on selected rows** list, select **Request Evidence**. Here, you can either create an evidence request or add more requests to an existing evidence request. The evidence request is created but not the evidence request tasks.

    Select **Create an evidence request task** in the **Request evidence** page to create request task.\[Omitted image "request\_evidence\_itam.png"\] Alt text: New evidence form.

-   From the following tables: Entity, Control, Control Objective, Control Test, Engagement, Issue. However, when the users request evidence from these tables, the evidence request is created, not the actual evidence request task. The users must go to the evidence request record that is generated and then add evidence request tasks.

In this procedure, the method to request evidence from the **My Evidence** module is described.

You can request evidence by using two different processes:

-   Three-step process \(standard\) The standard approach creates an Evidence Collection Details record as an intermediate step. This provides additional organization and context before evidence submission. → Continue with step 1 below.
-   Two-step process \(streamlined\) Skip the Evidence Collection Details step and move directly to evidence submission. Use this for simpler requests where collection instructions are minimal. → Jump to "Two-step process \(simplified\)" section below.

## Procedure

1.  Navigate to **Audit Workspace** &gt; **Engagement record \(in Validate state\)** &gt; **Evidence related list** and select **New**.

    The **New** button on the Evidence related list is shown in the example.

    \[Omitted image "evidence-new-button.png"\] Alt text: New button.

    The Request evidence form displays.

    \[Omitted image "req-evi-skip-colle-det-selected.png"\] Alt text: Skip collection detail.

2.  On the form, fill in the fields.

    To follow the two-step process, check the **Skip collection detail** check box.

    To follow the three-step process, leave the **Skip collection detail** check box unchecked.

<table id="table_u4n_4kk_lkc"><thead><tr><th>

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

Group assigned to provide evidence.Assigned toUser responsible for providing the evidence.

</td></tr><tr><td>

State

</td><td>

State of the request. The default state is Draft.

</td></tr><tr><td>

Type

</td><td>

The default type is Audit.

</td></tr><tr><td>

Request reason

</td><td>

Reason for requesting evidence.

</td></tr><tr><td>

Watch list

</td><td>

Users interested in viewing the evidence collected. If a person is added on the watch list, they can navigate to Audit &gt; Evidence Request &gt; Watched Evidence Requests to view the requests.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the evidence request.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the evidence request.

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

Type any notes that might be required..ContextThe table for the context record.

</td></tr><tr><td>

Activities

</td><td>

Activity log for the request.

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.

</td></tr><tr><td>

Context record

</td><td>

Context record for the evidence request.

</td></tr><tr><td>

Source

</td><td>

Object from where the evidence is initiated.

</td></tr><tr><td>

Skip collection detail

</td><td>

Option to create a two-step evidence request. Select the check box for a two-step process. Deselect for a three-step process. When you select this check box:-   The **Context** and **Evidence collection instructions** fields are hidden.
-   The **Description** field appears so that you can enter the evidence details.
-   The Evidence collection details related list is not created.
-   The request moves directly to **Work in Progress** state instead of Draft state.
-   A **New** button appears on the Evidence related list so that you can add evidence directly without creating collection details.


</td></tr><tr><td>

Evidence collection instructions

</td><td>

Instructions for evidence collection. Hidden when Skip collection detail check box is selected.

</td></tr></tbody>
</table>3.  Click **Request** in the Request evidence form.

    An Evidence request is created as shown in the example.

    \[Omitted image "evi-req-record-evi-rel-list.png"\] Alt text: Evidence related list.

4.  Follow these steps to create a response using two-step process \(if you selected the **Skip collection detail** check box in step 2\).

    1.  Click to open the Evidence request.

        In the Evidence request record, the **Details** tab shows that the **Skip collection detail** option is selected. The record is in **Work in progress** state. The work note shows that "Skip Collection" is enabled.

        \[Omitted image "evi-req-record-in-wip-state.png"\] Alt text: Evidence request in WIP state.

        A **New** button displays on the Evidence related list introduced as part of the two-step process as shown in the following example.

        \[Omitted image "evi-req-record-evi-rel-list-new-button.png"\] Alt text: New button.

    2.  Click the **New** button to open the Evidence form \(two-step\).

        The Evidence form is shown in the example.

        \[Omitted image "creating-response-by-selecting-new-button-in-evidence-rel-list.png"\] Alt text: Create a response.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the request.|
        |Type|The default type is Audit.|
        |Request reason|Reason for requesting evidence.|
        |Due date|Expected date of evidence submission.|
        |Context|Context for the evidence.|
        |Assignment group|Group assigned to the request.|
        |Assigned to|User assigned to the request.|
        |Evidence collection instructions|Evidence details and collection instructions \(appears only in two-step process\).|

    4.  Click **Request**.

        A message displays that the response is created.

        The Evidence related list shows the response.

        \[Omitted image "evi-response-created.png"\] Alt text: Evidence response created.

5.  Follow these steps to create a response using three-step process \(if you did not select the **Skip collection detail** check box in step 2\).

    After completing steps 2 and 3 \(with **Skip collection detail** check box unchecked\), another Evidence request is created.

    The **Details** tab of the Evidence request record shows that the record is in the **Draft** state, the **Skip collection detail** option is not selected, and the work note shows the activity details. A **New** button is not displayed on the Evidence related list.

    The Evidence collection details related list appears with a **New** button. This related list is used to list the items for which evidence is requested.

    \[Omitted image "3step-8-evi-req-record-then-skipcoldet-editable.png"\] Alt text: Skip collection detail editable.

    **Note:** If there are no Evidence collection details and the Evidence request record is in **Draft** state, the **Skip collection detail** field is editable. The field is not editable when the evidence request record is in the **Work in Progress** state. You can select the check box and follow the two-step process as outlined in step 4.

    1.  Select **New** in the Evidence collection details related list.

        |Field|Description|
        |-----|-----------|
        |Evidence request|Unique number of the evidence request task.|
        |Evidence for|Record for which evidence is requested.|
        |Assignment group|Group assigned to provide evidence. The users of this group must have the sn\_grc.business\_user roles.|
        |Assigned to|User responsible for providing evidence.|
        |Evidence collection instructions|Instructions for providing evidence. For example, list of supporting documents, files, and so on.|

    2.  Select **OK**.

    3.  Select **Submit**.

    4.  Select **Request Evidence**.

        When an evidence request is in Work in Progress and a new evidence collection detail is added, the evidence request task is sent to the assignee immediately.

        The Evidence related list appears with the list of evidences and the person who is assigned the request receives an email notification to provide the requested evidence. Also, the state of the request changes to **Work in Progress**.


