---
title: Get approval history and status in an MCP client
description: Retrieve the approval history and status for a quote approval by using natural language in a Model Context Protocol \(MCP\) client. You can use this information to review past approval decisions and check the progress of an in-progress approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/get-approval-history-mcp.html
release: australia
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 1
keywords: [MCP tools, approval history, quote approval, Advanced Approval Management AI]
breadcrumb: [Advanced Approval Management AI, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Get approval history and status in an MCP client

Retrieve the approval history and status for a quote approval by using natural language in a Model Context Protocol \(MCP\) client. You can use this information to review past approval decisions and check the progress of an in-progress approval.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Advanced Approval Management AI
-   Quote Management

Input required: Number of an active quote.

Role required: sn\_adv\_appr\_mgmt.approval\_request\_writer or sn\_adv\_appr\_mgmt.approver

## About this task

The Approval Details tool in Advanced Approval Management AI retrieves the approval activity for a quote. You can check the current status of a submitted quote and review decisions made during the approval process.

Enter a natural language request in your MCP client to run the tool.

## Procedure

1.  Open your MCP client application, which is connected to your ServiceNow instance using the Sales CRM Common Server.

2.  In your MCP client, enter a natural language request to get the approval history for a quote.

    The following examples show typical requests for retrieving the approval history:

    -   `Show me the approval history for quote QT0001006.`
    -   `What approvals have been completed for QT0001006?`
    -   `Who has approved quote QT0001006 so far?`
    -   `Who rejected this QT0001006 and why?`
    -   `Who recalled this quote?`
    -   `What is the full approval path for this quote?`
    The MCP client returns the approval history for the quote, which may include:

    -   The approvers who have acted on the quote
    -   The decision made by each approver \(for example, approved or rejected\)
    -   The date and time of each approval action
    -   Any comments or rejection reasons provided by approvers

## What to do next

Depending on your role and the state of the quote, you can submit the quote for approval if you're a requester. If you're an approver, you can approve or reject an approval request for a quote.

**Parent Topic:**[Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/use-advanced-approval-mgmt-ai.md)

