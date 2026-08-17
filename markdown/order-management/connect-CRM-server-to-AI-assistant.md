---
title: Connect Sales CRM server to an AI assistant
description: Connect the Sales CRM server to an AI assistant so that the assistant can manage advanced approval tasks directly from your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/connect-CRM-server-to-AI-assistant.html
release: australia
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management AI, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Connect Sales CRM server to an AI assistant

Connect the Sales CRM server to an AI assistant so that the assistant can manage advanced approval tasks directly from your ServiceNow instance.

## Before you begin

-   The Advanced Approval Management AI application is installed. For details, see [Install Advanced Approval Management AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-advanced-approval-management-ai.md).
-   Confirm that the Sales CRM server is enabled on your instance by navigating to **All** &gt; **MCP Server Console**. The Sales CRM server must be Active. If you don't see the server or want to create another MCP server, see [Create a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-mcp-server.md).
-   Confirm that the Advanced Approval Management AI tools are enabled on your instance by navigating to **All** &gt; **MCP Server Console** &gt; **Tools**. The following MCP tools must be Active \(set to True\):
    -   Approver Actions
    -   Get Approval Details
    -   Get Pending Approvals List
    -   Get Quote Details \(this is an MCP tool for Quote Management\)
    -   Requester Actions

Role required: admin or sn\_mcp\_server.admin

## Procedure

1.  Connect the Sales CRM server to your AI assistant.

    For instructions, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md).


