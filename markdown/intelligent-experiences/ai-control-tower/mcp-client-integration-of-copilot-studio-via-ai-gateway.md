---
title: AI Gateway setup and Client Registration
description: Setting up AI Gateway tab and creating MCP Client Registration.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Process flow of MCP servers Via AI Gateway, AI Gateway, Explore, AI Control Tower, Enable AI experiences]
---

# AI Gateway setup and Client Registration

Setting up AI Gateway tab and creating MCP Client Registration.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **AI assets** &gt; **AI asset inventory** &gt; **MCP servers**.

2.  Select and open an approved MCP server.

3.  Navigate to the **AI Gateway setup** tab.

    If an AI steward wants to enable ServiceNow Agent Studio for the approved MCP server, they can create a new MCP Client integration.

4.  Select **New** under **MCP Client integration**.

5.  Enter the **Name**.

    **Note:** A redirect URL will be available after an agent is created and configured. The redirect URL is a callback point endpoint used during OAuth.

    The redirect URL for the MCP clients is unique to each:

    -   AI Agent Studio: https://&lt;instance\_name&gt;.service-now.com/oauth\_redirect.do
    -   Copilot studio: Unique to the tool or connection that customers create inside their Copilot agent.
    -   Postman: https://oauth.pstmn.io/v1/browser-callback
    -   Other platforms: Consult the platform's OAuth documentation
6.  Select **Save**.


## Result

A connection to the MCP server is set up via AI Gateway.

**Note:** The Client ID and Client secret are automatically generated and available in the MCP server record. These credentials are used to authenticate the client when connecting to the Gateway.

To connect with Copilot Studio via AI Gateway, see [Connecting with Microsoft Copilot Studio Via AI Gateway](create-an-agent-in-copilot-studio-for-mcp-client-integration.md)

