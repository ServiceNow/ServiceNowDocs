---
title: Submit an approval request in an MCP client
description: Submit an entity such as a quote for approval or resubmit an entity that currently has no active approval request by using natural language in an MCP client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/submit-approval-request-mcp.html
release: australia
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management AI, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Submit an approval request in an MCP client

Submit an entity such as a quote for approval or resubmit an entity that currently has no active approval request by using natural language in an MCP client.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Advanced Approval Management AI
-   Quote Management

Input required: Number of an active quote.

Role required: sn\_adv\_appr\_mgmt.approval\_request\_writer

## About this task

Use the Requester Actions tool in Advanced Approval Management AI to submit a quote for approval or to resubmit an approval request that was previously rejected or recalled.

Enter a natural language request in your MCP client to run the tool.

## Procedure

1.  Open your MCP client application, which is connected to your ServiceNow instance using the Sales CRM Common Server.

2.  In your MCP client, enter a natural language request to submit a quote for approval.

    The following examples show typical requests for submitting a quote for approval for the first time:

    -   `Submit quote QT0001006 for approval`
    -   `Send QT0001006 for approval`
    -   If you're currently chatting about a particular quote, enter `Submit this quote for approval` or `This quote is ready, get it approved`
    The MCP client submits the approval request for the quote and creates the approval request record. Notifications to approvers and requesters are generated, informing them of the approval request.


**Parent Topic:**[Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/use-advanced-approval-mgmt-ai.md)

