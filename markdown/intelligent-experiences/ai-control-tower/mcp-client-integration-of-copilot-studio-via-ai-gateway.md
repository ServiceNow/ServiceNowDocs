---
title: Configure Client registration and AI Gateway Setup
description: Explore MCP Client registration and AI Gateway Setup.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/mcp-client-integration-of-copilot-studio-via-ai-gateway.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Process flow of MCP Servers Via AI Gateway, AI Gateway, Explore, AI Control Tower, Enable AI experiences]
---

# Configure Client registration and AI Gateway Setup

Explore MCP Client registration and AI Gateway Setup.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **AI assets** &gt; **AI asset inventory** &gt; **MCP servers**.

2.  Select and open an approved MCP server.

3.  Navigate to the **AI Gateway setup** tab.

    If an AI steward wants to enable AI Agent Studio for the approved MCP server, they can create MCP Client integration.

4.  Under **MCP Client integration**, select **New**.

5.  Enter the **Name**.

    **Note:** A redirect URL will be available after an agent is created and configured. The redirect URL is a callback endpoint used during OAuth.

    The redirect URL for the MCP clients is unique to each:

    -   AI Agent Studio: https://&lt;instance\_name&gt;.service-now.com/oauth\_redirect.do
    -   Copilot studio: Unique to the tool or connection that you can create inside your Copilot agent
    -   Postman: https://oauth.pstmn.io/v1/browser-callback
    -   Other platforms: Consult the platform's OAuth documentation
6.  Select **Save**.


## Result

A connection to an MCP server is set up via the AI Gateway.

**Note:** The Client ID and Client secret are automatically generated and available in the MCP server record. These credentials are used to authenticate the client when connecting to the AI Gateway.

To connect with Copilot Studio via AI Gateway, see [Connecting with Microsoft Copilot Studio Via AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

