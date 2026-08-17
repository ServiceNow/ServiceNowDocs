---
title: Using Advanced Approval Management AI
description: Advanced Approval Management AI enables approval requesters and approvers to manage quote approvals using natural language requests in an MCP client, without opening a ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/use-advanced-approval-mgmt-ai.html
release: australia
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 2
keywords: [use]
breadcrumb: [Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Using Advanced Approval Management AI

Advanced Approval Management AI enables approval requesters and approvers to manage quote approvals using natural language requests in an MCP client, without opening a ServiceNow instance.

## Using Advanced Approval Management AI tools in the quote approval workflow

Approval users use the chat feature in the MCP client to perform, manage, and track the approval steps that use the MCP tools provided with Advanced Approval Management AI.

-   **Using MCP tools as a requester \(sales rep\)**

    As part of managing quote approvals, including submitting them for approval, requesters can do the following using an MCP client:

    1.  Before submitting a quote, get quote details to review the current state of the quote.

        The requester can prompt to see quote header details and line details, for example to check discounts applied and quote composition if there are multiple lines.

    2.  Request an approval preview to see the approvers, approval rules, and the approval routing required for the quote.

        The requester can determine whether the quote meets the approval rules and any conditions, such as margin limits or specific regulatory guidelines, before submitting a quote for approval.

    3.  If needed, add an ad-hoc approver for an approval rule relevant to the quote.
    4.  Submit the quote for approval with a comment.
    5.  Recall an approval request for the quote to make any changes to the quote.
    6.  Update a quote that has been recalled or was rejected, then resubmit for approval.
-   **Using MCP tools as approver**

    As part of approving or rejecting quotes, approvers can do the following using an MCP client:

    1.  Request pending approvals to identify quotes that require action.
    2.  Request quote header and line details to review the quote.
    3.  Optionally request approval history to review previous decisions on the quote.
    4.  If needed, add an ad-hoc approver for an approval rule relevant to the quote.
    5.  Act on an approval request by approving or rejecting the quote with a comment.

-   **[Get quote details in an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/get-quote-details-mcp.md)**  
Retrieve quote header and line-level information using natural language in a Model Context Protocol \(MCP\) client.
-   **[Get approval history and status in an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/get-approval-history-mcp.md)**  
Retrieve the approval history and status for a quote approval by using natural language in a Model Context Protocol \(MCP\) client. You can use this information to review past approval decisions and check the progress of an in-progress approval.
-   **[Preview approval routing in an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/get-approval-preview-mcp.md)**  
View the approval routing to be triggered for a quote that has not been submitted for approval by using natural language in a Model Context Protocol \(MCP\) client. You can view the approval rules to be applied and the assigned approvers in the routing sequence.
-   **[Submit an approval request in an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/submit-approval-request-mcp.md)**  
Submit an entity such as a quote for approval or resubmit an entity that currently has no active approval request by using natural language in an MCP client.

**Parent Topic:**[Using configure, price, quote applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-cpq.md)

**Related topics**  


[Configuring Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-advanced-approval-mgmt-ai.md)

