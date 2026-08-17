---
title: Preview approval routing in an MCP client
description: View the approval routing to be triggered for a quote that has not been submitted for approval by using natural language in a Model Context Protocol \(MCP\) client. You can view the approval rules to be applied and the assigned approvers in the routing sequence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/get-approval-preview-mcp.html
release: australia
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [MCP tools, approval preview, Get Approval Preview, approval routing, quote approval, Advanced Approval Management AI]
breadcrumb: [Advanced Approval Management AI, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Preview approval routing in an MCP client

View the approval routing to be triggered for a quote that has not been submitted for approval by using natural language in a Model Context Protocol \(MCP\) client. You can view the approval rules to be applied and the assigned approvers in the routing sequence.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Advanced Approval Management AI
-   Quote Management

Input: Quote number of the quote you want to preview.

Role required:sn\_adv\_appr\_mgmt.approval\_request\_writer

## About this task

Use the Approval History tool in Advanced Approval Management AI to see the approval routing that will be triggered for a quote approval. You can then determine whether to adjust your quote before submitting it for approval.

You don't invoke the tool directly. Instead, enter a conversational request in your MCP client, which calls the tool for you.

## Procedure

1.  Open your MCP client application such as Claude, which is connected to your ServiceNow instance using the Sales CRM Common Server.

2.  In your MCP client, start a chat by entering a natural language request about the approval routing for a quote.

    For example:

    -   `What will happen when this request is submitted?`
    -   `Show me the approval routing for quote QT0001006.`
    -   `Who will approve quote QT0001006?`
    -   `Preview approvals for QT0001006 before I submit.`
    The MCP client returns the approval routing information for the quote, which includes:

    -   The approval chain, for example a Finance chain and the order of steps in the chain.
    -   The approval rule \(condition\) that triggers the approvers for your request and the routing sequence.
    -   The approvers in the routing sequence and their approval status.


3.  Indicate whether you want to submit the request for approval.

    -   To submit the approval request, enter `Yes, go ahead and submit the quote for approval`.

        Your quote is submitted for approval. Your quote is in the Pending state until the first approver approves or rejects your request.

    -   If you want to make further changes to your quote, enter `Update quote`. The client asks if you like to review quote details. You can review the details. Next, if needed, update the quote, perhaps to make pricing adjustments to the quote in your ServiceNow instance.


**Parent Topic:**[Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/use-advanced-approval-mgmt-ai.md)

