---
title: Submit an approval request in an MCP client
description: Submit an entity such as a quote for approval or resubmit an entity that currently has no active approval request by using natural language in an MCP client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/submit-approval-request-mcp.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [MCP tools, submit for approval, Requestor Actions, quote approval]
breadcrumb: [Advanced Approval Management AI, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Submit an approval request in an MCP client

Submit an entity such as a quote for approval or resubmit an entity that currently has no active approval request by using natural language in an MCP client.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Advanced Approval Management AI
-   Quote Management

Input required: Number of a quote in the Draft or Rejected state.

Role required: sn\_adv\_appr\_mgmt.approval\_request\_writer and sn\_quote\_mgmt\_core.quote\_writer

## About this task

Use the Requestor Actions tool in Advanced Approval Management AI to submit a quote for approval or to resubmit an approval request that was previously rejected or recalled.

Preview the approval routing before you submit. For more information, see [Preview approval routing in an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/get-approval-preview-mcp.md).

Enter a natural language request in your MCP client to run the tool.

## Procedure

1.  Open your MCP client application, which is connected to your ServiceNow instance using the Sales CRM Common Server.

2.  In your MCP client, enter a natural language request to submit a quote for approval.

    The following examples show typical requests for submitting a quote for approval for the first time:

    -   `Submit quote QT0001006 for approval`
    -   `Send QT0001006 for approval`
    -   If you're currently chatting about a particular quote, enter `Submit this quote for approval` or `This quote is ready, get it approved`
    The MCP client submits the quote for approval. The quote state changes to Requested for review, an approval request is created, and the first approvers are notified. If no approval rule applies, the quote is approved without an approval request.

    **Note:** If the quote already has a pending approval request or isn't in the Draft or Rejected state, it isn't submitted again, and the client tells you the quote's current state.

    **Note:** If you don't have write access to the quote, the approval request is created but the quote state doesn't change.


**Parent Topic:**[Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/use-advanced-approval-mgmt-ai.md)

