---
title: Classic approvals
description: Classic approvals are records that store the authorization tasks that must be done to approve or reject a request. Approval records are typically created by a Workflow Studio flow or classic workflow. An approval defines both the approval tasks and the users or groups are assigned to approve or reject them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/approvals/r\_Approvals.html
release: australia
product: Approvals
classification: approvals
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Build workflows]
---

# Classic approvals

Classic approvals are records that store the authorization tasks that must be done to approve or reject a request. Approval records are typically created by a Workflow Studio flow or classic workflow. An approval defines both the approval tasks and the users or groups are assigned to approve or reject them.

Administrators create approval logic from Workflow Studio flows or classic workflows.

-   Create a Workflow Studio flow that contains an [Ask for Approval action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/ask-approval-flow-designer.md).
-   Create a classic workflow that contains either an [Approval - Group workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-activities/r_ApprovalGroup.md) or an [Approval - User workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-activities/r_ApprovalUser.md).

In either case, the approval record defines this information.

-   The record type that needs approval. For example, a Service Catalog request or a change request.
-   The people who can approve or deny the approval request. For example, a specific assignment group or a user's manager.
-   The approval rules that determine how multiple approval decisions interact. For example, an approval that requires all approval users to respond or an approval where any single person can approve or reject an approval request.

Users can see their approval requests by navigating to **All** &gt; **Self-Service** &gt; **My Approvals**.

## Approval record

An approval record consists of these fields:

<table id="table_dkw_tvt_lt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approver

</td><td>

A reference to the user who is responsible for approving the related record.

</td></tr><tr><td>

State

</td><td>

Choices are: -   Not Yet Requested \(This state indicates that you aren't yet asking your approval users to approve this request. Until you set the status to **Requested** they will receive no email notifications about the request.\)
-   Requested
-   Approved
-   Rejected

</td></tr><tr><td>

Approving

</td><td>

A document\_id reference field to the record being approved, on any table.

</td></tr><tr><td>

Comments

</td><td>

A journal field for storing comments regarding the approval.

</td></tr><tr><td>

Approval Summarizer

</td><td>

A [Create a formatter and add it to a form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAFormatter.md) that displays key fields relevant to the approval from the referenced document. This summarizer will not display if there is no record referenced.

</td></tr></tbody>
</table>