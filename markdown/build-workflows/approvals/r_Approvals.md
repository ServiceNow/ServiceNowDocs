---
title: Classic approvals
description: Classic approvals are a legacy process to require authorization on tasks before the work is done. In earlier releases, you could create approval records to define approval tasks and associate users or groups to approve or reject them.
locale: en-US
release: australia
product: Approvals
classification: approvals
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build workflows]
---

# Classic approvals

Classic approvals are a legacy process to require authorization on tasks before the work is done. In earlier releases, you could create approval records to define approval tasks and associate users or groups to approve or reject them.

Administrators can define classic approval logic by navigating to **All** &gt; **System Policy** &gt; **Rules** &gt; **Approvals**.

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](../../flow-designer/reference/ask-approval-flow-designer.md). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

Administrators can see all approval requests by navigating to **All** &gt; **Self-Service** &gt; **My Approvals** and removing the list filter.

An approval record consists of these fields:

<table id="table_dkw_tvt_lt"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Approver

</td><td>

A reference to the user who is responsible for approving the related record.

</td></tr><tr><td>

State

</td><td>

Choices are: -   Not Yet Requested \(This state indicates that you are not yet asking your approvers to approve this request. Until you set the status to **Requested** they will receive no email notifications about the request.\)
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

A [Create a formatter and add it to a form](https://www.servicenow.com/docs/access?context=t_CreateAFormatter&version=australia&pubname=australia-platform-administration&ft:locale=en-US) that displays key fields relevant to the approval from the referenced document. This summarizer will not display if there is no record referenced.

</td></tr></tbody>
</table>