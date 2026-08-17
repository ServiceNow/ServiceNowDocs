---
title: Get quote details in an MCP client
description: Retrieve quote header and line-level information using natural language in a Model Context Protocol \(MCP\) client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/get-quote-details-mcp.html
release: australia
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 2
keywords: [MCP tools, quote details, quote header, quote lines, Advanced Approval Management AI]
breadcrumb: [Advanced Approval Management AI, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Get quote details in an MCP client

Retrieve quote header and line-level information using natural language in a Model Context Protocol \(MCP\) client.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Advanced Approval Management AI
-   Quote Management

Input required: Number of an active quote.

Role required: sn\_adv\_appr\_mgmt.approval\_request\_writer or sn\_adv\_appr\_mgmt.approver

## About this task

The Get Quote Details tool enables you to retrieve information from a quote header and quote lines in an MCP client. Header-level detail includes the quote status, approval state, and key quote attributes. Line-level detail includes the individual products, quantities, and pricing on the quote. You can specify the level of detail in your natural language prompt. Or you can simply enter the quote number to return both header and line details.

## Procedure

1.  Open your MCP client application, which is connected to your ServiceNow instance using the Sales CRM Common Server.

2.  In your MCP client, enter a natural language request to get details for a quote.

    The following examples show typical requests for retrieving quote details and the level of detail:

    -   To request header and line-level details:
        -   `Get the details for quote QT0001006.`
        -   `Show me the header and line details for quote QT0001006.`
    -   For line-level details: `Get the line details for quote QT0001006.`
    -   For other quote details:
        -   `What is the MRR for quote QT0001006?`
        -   `What is the state of quote QT0001006?`
3.  Review the quote details returned.

    For header-level requests, the MCP client returns information such as:

    -   Quote number and name
    -   Quote status and approval state
    -   Account and opportunity details
    -   Quote owner and creation date
    For line-level requests, the MCP client returns information such as:

    -   Product names and catalog item details
    -   Quantities and unit prices
    -   Discounts and net amounts
    -   Line-level approval status

## Get quote details

\[Omitted image "get-quote-details-mcp-chat.png"\] Alt text: Chat that shows the quote header and line details returned and the suggested next action to preview approval routing for the

## What to do next

The MCP client considers the next approval activity in a typical approval workflow that you might want to take, depending on your role and the quote state.

For example:

-   If you're a requester and the quote has not been submitted for approval, the MCP client asks if you want to preview the approval routing for the quote. If the quote is in a rejected state, the MCP client asks if you want to see the approval history. You can view the rejection reason so that you can update the quote accordingly before resubmitting the quote for approvals.
-   If you're an approver, the MCP client asks if you want to see your pending approvals so that you can take action on your approval requests.

**Parent Topic:**[Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/use-advanced-approval-mgmt-ai.md)

