---
title: Get approval history and status in an MCP client
description: Retrieve the approval history and status for a quote approval by using natural language in a Model Context Protocol \(MCP\) client. You can use this information to review past approval decisions and check the progress of an in-progress approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/get-approval-history-mcp.html
release: brazil
topic_type: task
last_updated: "2026-11-16"
reading_time_minutes: 1
keywords: [MCP tools, approval history, quote approval, Advanced Approval Management AI, ServiceNow Otto for Advanced Approval Management]
breadcrumb: [Advanced Approval Management AI, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Get approval history and status in an MCP client

Retrieve the approval history and status for a quote approval by using natural language in a Model Context Protocol \(MCP\) client. You can use this information to review past approval decisions and check the progress of an in-progress approval.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Advanced Approval Management AI
-   Quote Management

Input required: Number of an active quote.

To read the quote, you also need the sn\_quote\_mgmt\_core.quote\_viewer role.

Role required: sn\_adv\_appr\_mgmt.approval\_request\_approver or sn\_adv\_appr\_mgmt.approval\_request\_writer

## About this task

The Get Approval Details tool in Advanced Approval Management AI retrieves the approval activity for a quote. You can check the current status of a submitted quote and review decisions made during the approval process.

The history covers the approval requests for the current version of the quote. Earlier quote versions aren't included.

Enter a natural language request in your MCP client to run the tool.

## Procedure

1.  Open your MCP client application, which is connected to your ServiceNow instance using the Sales CRM Common Server.

2.  In your MCP client, enter a natural language request to get the approval history for a quote.

    The following examples show typical requests for retrieving the approval history:

    -   `Show me the approval history for quote QT0001006.`
    -   `What approvals have been completed for QT0001006?`
    -   `Who has approved quote QT0001006 so far?`
    -   `Who rejected quote QT0001006?`
    -   `Who recalled this quote?`
    -   `What is the full approval path for this quote?`
    The MCP client returns each approval request for the quote, newest first. For each request, the client shows the following information:

    -   The request number and state.
    -   Who requested the approval and when.
    -   Whether the request was recalled or rejected.
    -   Each approval step, with its approval chain, approval rule, trigger condition, step state, assigned approver, the approver who acted, and the dates.

## What to do next

To act on the approval, see  or .

**Parent Topic:**[Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/use-advanced-approval-mgmt-ai.md)

