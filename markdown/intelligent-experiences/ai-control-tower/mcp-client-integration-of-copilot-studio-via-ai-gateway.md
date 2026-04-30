---
title: Setting up for connections with AI Gateway
description: Setting up the connections with AI Gateway.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Process flow of MCP servers Via AI Gateway, Explore AI Gateway, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Setting up for connections with AI Gateway

Setting up the connections with AI Gateway.

## Before you begin

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

## Procedure

1.  Navigate to **AI assets** &gt; **AI asset inventory** &gt; **MCP servers**.

2.  Select and open the approved request.

3.  Navigate to the **AI Gateway setup** tab.

4.  Select **New** under **MCP Client integration**.

5.  Enter the **Name**.

    **Note:** A redirect URL will be available after an agent is created and configured. The redirect URL for the MCP Clients is unique to each:

    AI Agent Studio- &lt;instance\_url&gt;/oauth\_redirect.do.

    Copilot studio- Unique to the tool or connection that customers create inside their Copilot agent.

6.  Select **Save**.


## Result

A connection to the MCP server is set up via AI Gateway.

**Note:** The Client ID and Client secret are generated and available in the MCP server record. Using the Client ID and Client secret, you can connect to the MCP server via AI Gateway.

To connect with Copilot Studio via AI Gateway, see [Connecting with Copilot Studio Via AI Gateway](create-an-agent-in-copilot-studio-for-mcp-client-integration.md)

