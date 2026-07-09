---
title: Advanced Approval Management AI
description: The ServiceNow Advanced Approval Management AI application brings quote approval capabilities to Model Context Protocol \(MCP\)-compatible clients. Advanced approval users can manage quote approvals using natural language requests in an MCP client, without opening a ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/explore-advanced-approval-mgmt-ai.html
release: australia
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 3
keywords: [Advanced Approval Management AI, MCP tools, Model Context Protocol, quote approvals, Sales CRM MCP server, explore]
breadcrumb: [Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Advanced Approval Management AI

The ServiceNow® Advanced Approval Management AI application brings quote approval capabilities to Model Context Protocol \(MCP\)-compatible clients. Advanced approval users can manage quote approvals using natural language requests in an MCP client, without opening a ServiceNow instance.

## Advanced Approval Management AI overview

Advanced Approval Management AI provides MCP tools that enable approval users to engage in approval activities using the chat feature of an MCP client such as Claude. The MCP tools retrieve quote and approval request information from the Sales CRM server, which connects the MCP client to a ServiceNow instance.

Approval requesters and approvers enter prompts or queries in the MCP client, such as asking for quote details or submitting an approval request for approval. The MCP client runs the appropriate MCP tool functionality for Advanced Approval Management AI, and returns the result.

## MCP tools for Advanced Approval Management AI

<table id="table_ihv_tsc_tjc"><thead><tr><th>

Tool name \[ID\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval Actions \(sn\_qut\_sum\_skill.approval\_actions\)

</td><td>

Submits a quote for approvals and routes them to assigned approvers.

</td></tr><tr><td>

Approval Details \(sn\_adv\_apr\_mgt\_ai.approval\_details\)

</td><td>

Retrieves the complete approval cycle history for a quote, including every approval request, step, approval actions, any recalls or rejections.

</td></tr><tr><td>

Get Approval Preview \(sn\_qut\_sum\_skill.get\_approval\_preview \)

</td><td>

Previews the approval routing for a quote before a requester submits the quote for approval.

</td></tr><tr><td>

Get pending approval list \(sn\_adv\_apr\_mgt\_ai.get\_pending\_approval\_list\)

</td><td>

Retrieves all approval requests pending for an approver.

</td></tr><tr><td>

Get Quote Details \(sn\_qut\_sum\_skill.get\_quote\_details\)

</td><td>

Retrieves quote header and line item details.

</td></tr><tr><td>

Update approval request \(sn\_adv\_apr\_mgt\_ai.update\_approval\_request\)

</td><td>

Executes approve or reject actions on pending approval steps assigned to an approver.

</td></tr></tbody>
</table>## Advanced Approval Management AI users

|User|Description|
|----|-----------|
|Requester \(sales rep\)|Submits sales quotes for approval and tracks the status of approval requests as they move through the approval workflow. Accesses quote details and approval history to track approval request status.|
|Approver|Reviews and approves or rejects requests for quote approval. Accesses quote details and approval history to track approval request status.|
|Admin|Installs the required plugins and assigns the MCP server roles to requesters and approvers.|

## Advanced Approval Management AI workflow

Requesters and approvers manage the quote approval process by entering a series of queries or prompts in the MCP client, to get information or perform an approval-related task, such as submitting a quote or approving a request. The client returns requested information and performs requested actions, then provides a summary of information requested or confirmation that the task was completed.

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

With Advanced Approval Management AI, your approval users can perform approval tasks with improved efficiency by using the conversational interface of the MCP client, instead of navigating between multiple options and forms or switching between tools during the sales cycle.

## What to explore next

To learn more about configuring and using Advanced Approval Management AI, see:

-   Configuring Advanced Approval Management AI
-   Using Advanced Approval Management AI
-   Advanced Approval Management AI reference

