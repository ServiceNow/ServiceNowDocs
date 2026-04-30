---
title: Classic approvals
description: Classic approvals are a legacy process to require authorization on tasks before the work is done. In earlier releases, you could create approval records to define approval tasks and associate users or groups to approve or reject them.
locale: en-US
release: zurich
product: Approvals
classification: approvals
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Classic approvals

Classic approvals are a legacy process to require authorization on tasks before the work is done. In earlier releases, you could create approval records to define approval tasks and associate users or groups to approve or reject them.

Administrators can define classic approval logic by navigating to **All** &gt; **System Policy** &gt; **Rules** &gt; **Approvals**.

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](https://www.servicenow.com/docs/access?context=ask-approval-flow-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

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

A [Create a formatter and add it to a form](https://www.servicenow.com/docs/access?context=t_CreateAFormatter&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) that displays key fields relevant to the approval from the referenced document. This summarizer will not display if there is no record referenced.

</td></tr></tbody>
</table>-   **[Approval engines](../concept/c_ApprovalEngines.md)**  
The differences in the way that companies handle their approvals, as well as the differences between approvals for the various applications \(such as Service Catalog Requests and Change Management\), calls for supporting flexibility in setting up approvals within applications.
-   **[Approval rules](../concept/c_ApprovalRules.md)**  
Many organizations rely on an approval process to ensure that requests are reasonable and fit an organization's budget.
-   **[Approval summarizer formatter](r_ApprovalSummarizerFormatter.md)**  
The approval summarizer formatter creates the summary at the bottom of an approval form.
-   **[Approval with e-signature](../concept/approval-with-e-signature.md)**  
Approve or reject an approval record by re-entering your login credentials. See the history of an approval from its activity stream or its audit history.
-   **[Approval status](../concept/c_ApprovalStatus.md)**  
The approval status of a change request is determined by looking at the current status of all the approvers.
-   **[Generate an approval using approval rules](../concept/c_GenAnApprovalUsingApprRules.md)**  
The system can automatically generate an approval request to individuals or groups when specific criteria are met. The automatic generation of approval requests is driven using the System Policy feature.
-   **[Generate approvals using the approvers related list](../concept/c_GenApprovalsUsingApprsRelList.md)**  
It is possible to manually add approvers to a request.
-   **[Generate approvals using Workflow flows](../concept/c_GeneApprovalsUsingWorkflows.md)**  
Workflow Studio flows are a powerful and flexible method of generating approvals. Use workflow flows to create group approvals and user approvals.
-   **[Multiple approvers](../concept/c_MultipleApprovers.md)**  
With multiple approvers, all approvers must authorize the request before the status will change to "Approved".
-   **[Receive notifications](../concept/c_ReceiveNotifications.md)**  
Individuals who are designated approvers automatically receive approval notifications, including approval status updates.
-   **[Dynamic approval forms](../concept/c_DynamicApprovalForms.md)**  
When you are looking at an approval request, the form has a context-appropriate summary of the item to be approved.
-   **[Scripts and engines execution order](execution-order-scripts-engines.md)**  
Scripts, assignment rules, business rules, workflows, escalations, and engines all take effect in relation to a database operation, such as insert or update. In many cases, the order of these events is important.

**Parent Topic:**[Exploring Service Administration](../concept/c_ServiceAdministration.md)

