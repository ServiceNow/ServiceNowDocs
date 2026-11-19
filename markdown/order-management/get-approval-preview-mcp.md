---
title: Preview approval routing in an MCP client
description: View the approval routing to be triggered for a quote that has not been submitted for approval by using natural language in a Model Context Protocol \(MCP\) client. You can view the approval rules to be applied and the assigned approvers in the routing sequence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/get-approval-preview-mcp.html
release: brazil
topic_type: task
last_updated: "2026-11-13"
reading_time_minutes: 2
keywords: [MCP tools, approval preview, Get Approval Details, approval routing, quote approval, Advanced Approval Management AI, ServiceNow Otto for Advanced Approval Management]
breadcrumb: [Advanced Approval Management AI, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Preview approval routing in an MCP client

View the approval routing to be triggered for a quote that has not been submitted for approval by using natural language in a Model Context Protocol \(MCP\) client. You can view the approval rules to be applied and the assigned approvers in the routing sequence.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Advanced Approval Management AI
-   Quote Management

Input required: Quote number of a quote in the Draft state.

To read a quote, you need the sn\_quote\_mgmt\_core.quote\_viewer role. To submit the quote, you also need the sn\_adv\_appr\_mgmt.approval\_request\_writer and sn\_quote\_mgmt\_core.quote\_writer roles.

Role required: sn\_adv\_appr\_mgmt.approval\_request\_viewer

## About this task

Use the Get Approval Details tool in Advanced Approval Management AI to see the approval routing that would be triggered if you submitted the quote now. Previewing doesn't submit the quote or change its state. You can then decide whether to adjust your quote before you submit it for approval.

You don't invoke the tool directly. Instead, enter a conversational request in your MCP client, which calls the tool for you.

If the quote isn't in the Draft state, the client indicates that previews are available only for Draft quotes. The same message may appear if you don't have read access to the quote.

## Procedure

1.  Open your MCP client application such as Claude, which is connected to your ServiceNow instance using the Sales CRM Common Server.

2.  In your MCP client, start a chat by entering a natural language request about the approval routing for a quote.

    For example:

    -   `What will happen when this request is submitted?`
    -   `Show me the approval routing for quote QT0001006.`
    -   `Who will approve quote QT0001006?`
    -   `Preview approvals for QT0001006 before I submit.`
    The MCP client returns the approval routing for the quote, grouped by approval chain in chain order. For each approval rule, it shows the rule name, the trigger condition that the quote matches, the approvers or approval groups, and whether any one or all approvers must approve. All approvals show the Not yet requested state.

    **Note:** Approval rules that don't resolve to any approver aren't included. An approval group appears once in the preview; when you submit, each active group member receives an approval. If no approval rule applies, the client tells you that no approval is required and the quote would be approved when you submit it.

3.  Indicate whether you want to submit the request for approval.

    -   To submit the approval request, enter `Yes, go ahead and submit the quote for approval`.

        Your quote is submitted for approval and its state changes to Requested for review.

    -   If you want to make further changes to your quote, enter `Update quote`. The client asks if you like to review quote details. You can review the details. Next, if needed, update the quote, perhaps to make pricing adjustments to the quote in your ServiceNow instance.

**Parent Topic:**[Using Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/use-advanced-approval-mgmt-ai.md)

**Related topics**  


[Submit an approval request in an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/submit-approval-request-mcp.md)

