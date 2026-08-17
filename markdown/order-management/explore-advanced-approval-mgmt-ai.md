---
title: Advanced Approval Management AI
description: The ServiceNow Advanced Approval Management AI application brings quote approval capabilities to Model Context Protocol \(MCP\)-compatible clients. Advanced approval users can manage quote approvals using natural language requests in an MCP client, without opening a ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/explore-advanced-approval-mgmt-ai.html
release: australia
topic_type: concept
last_updated: "2026-08-07"
reading_time_minutes: 3
keywords: [Advanced Approval Management AI, MCP tools, Model Context Protocol, quote approvals, Sales CRM MCP server, explore]
breadcrumb: [Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Advanced Approval Management AI

The ServiceNow® Advanced Approval Management AI application brings quote approval capabilities to Model Context Protocol \(MCP\)-compatible clients. Advanced approval users can manage quote approvals using natural language requests in an MCP client, without opening a ServiceNow instance.

## Advanced Approval Management AI overview

Advanced Approval Management AI provides MCP tools that enable approval users to engage in approval activities using the chat feature of an MCP client such as Claude. The MCP tools retrieve quote and approval information from the Sales CRM server, which connects the MCP client to a ServiceNow instance.

Approval requesters and approvers enter prompts and queries in the chat interface of the MCP client, without navigating through application menus and forms in the ServiceNow instance. For example requesters or approvers can ask for the approval history for a quote or get quote details. The MCP client runs the appropriate Advanced Approval Management AI MCP tool functionality, then returns the result.

Your requesters \(sales reps\) and approvers can do the following advanced approval tasks by entering natural language prompts in the MCP client interface.

<table id="table_nf3_hvf_vjc"><thead><tr><th>

Approval activity

</th><th>

User role

</th><th>

Example query or prompt

</th></tr></thead><tbody><tr><td>

Get quote details, such as header and line items

</td><td>

Requester or approver

</td><td>

-   `Get me info on QT0001035`
-   `I need header details on QT0001035`

</td></tr><tr><td>

Preview the approvals required for a quote, such as the approval rules and approvers

</td><td>

Requester

</td><td>

-   `Who are the approvers for QT0001035?`
-   `What is the business rule for QT0001035?`

</td></tr><tr><td>

Submit quote for approval

</td><td>

Requester

</td><td>

`Submit QT0001035 for approval`

</td></tr><tr><td>

Retrieve the complete approval cycle history for a quote \(including every approval request, step, approval actions, any recalls or rejections\)

</td><td>

Requester or approver

</td><td>

-   `What is the history for QT0001035?`
-   `What is happening with QT0001035?`
-   `Who approved QT0001035?`

</td></tr><tr><td>

Retrieve all pending approval requests

</td><td>

Approver

</td><td>

`What requests do I need to approve?`

</td></tr><tr><td>

Executes approve or reject actions on pending approval steps

</td><td>

Approver

</td><td>

`Approve this step`

</td></tr></tbody>
</table>## Advanced Approval Management AI users

|User|Description|
|----|-----------|
|Requester \(sales rep\)|Submits sales quotes for approval and tracks the status of approval requests as they move through the approval workflow. Accesses quote details and approval history to track approval request status.|
|Approver|Reviews and approves or rejects requests for quote approval. Accesses quote details and approval history to track approval request status.|
|Admin|Installs the required plugins and assigns the MCP server roles to requesters and approvers.|

## Advanced Approval Management AI workflow

Requesters and approvers manage the quote approval process by entering a series of queries or prompts in the chat interface of an MCP client. For example, approval activities can include getting quote information or performing a task, such as submitting a quote for approval. The client returns requested information and performs requested actions, then provides a summary of information requested or confirmation that the task was completed.

The following describes a typical end-to-end workflow.

1.  The sys admin installs the required plugins and assigns the MCP-related roles to advanced approval users.
2.  Requesters and approvers connect their MCP-compatible client to the Sales CRM Server.
3.  The requester asks for quote details to review the current state of a quote.
4.  The requester requests an approval preview of the quote to see the approval routing, approval rules, and approvers, before submitting a quote.
5.  The requester submits the quote for approval.
6.  The approver asks for a list of their pending approvals list to identify and prioritize quote approval requests that require action.
7.  The approver retrieves the quote header and line details and optionally reviews the approval history for the quote.
8.  The approver approves or rejects the request. If the quote is rejected, the approver must supply a comment that explains the reason for rejection.

## Advanced Approval Management AI benefits

With Advanced Approval Management AI, your approval users can perform approval tasks with improved efficiency by using the conversational interface of an MCP client, instead of navigating between multiple options and forms to complete tasks or switch between tools during the sales cycle.

## What to explore next

To learn more about configuring and using Advanced Approval Management AI, see:

-   [Configuring Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-advanced-approval-mgmt-ai.md)
-   [Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/use-advanced-approval-mgmt-ai.md)
-   [Components installed with Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-with-advanced-approval-mgmt-AI.md)

