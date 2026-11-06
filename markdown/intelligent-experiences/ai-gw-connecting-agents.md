---
title: Connecting agents through AI Gateway
description: Register the clients that can connect to an approved MCP server, and then configure agents to call the server through its AI Gateway MCP server URL.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-connecting-agents.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, use, MCP client, CIMD client, AI Gateway MCP server URL]
breadcrumb: [AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Connecting agents through AI Gateway

Register the clients that can connect to an approved MCP server, and then configure agents to call the server through its AI Gateway MCP server URL.

## Overview of connecting agents

An agent connects to an MCP server through AI Gateway in two stages:

1.  An AI steward registers a client for the server, which gives the agent platform its OAuth credentials.
2.  The agent owner configures the agent with the server's AI Gateway connection details and the client's credentials.

Before you start, the MCP server must be in the inventory and approved:

-   To add the server to the inventory, see [Add an MCP server from AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-an-mcp-server-from-ai-agent-studio.md), [Add an MCP server from MCP Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-add-an-mcp-server-from-mcp-catalog.md), or [Add an MCP server from AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-add-an-mcp-server-from-ai-control-tower.md). For an overview of the ways to add a server, see [MCP server setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mcp-server-setup.md).
-   To approve the server, see [MCP server approval playbook workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-mcp-server-approval-playbook-workflow.md). When the server is approved, the record's header shows **Deployed &amp; Approved**. Until then, the record's **AI Gateway** tab shows that the server hasn't been approved.

## Register a client

You register clients on the server's record. In AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers**, select the server name, select the **AI Gateway** tab, and then select the **Setup** sub-tab. The **CIMD and MCP client integration** panel lists the clients registered for the server. If the server has more than one variant, select the variant from the list first. Select **Add client**, and then choose the client type. **MCP client** is selected by default.

Choose the client type based on the agent platform:

|Client type|Use it for|What you provide|Details|
|-----------|----------|----------------|-------|
|CIMD client|Clients that publish a Client ID Metadata Document. Supported for VS Code.|The URL of the client's metadata document, as the client ID. After you select **Validate**, you set the sync mode, redirect URLs, logo URL, and security controls, and AI Gateway creates the OAuth client.|[Add a CIMD client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-a-cimd-client.md)|
|MCP client|All other platforms, such as AI Agent Studio, Postman, Claude Desktop, and Microsoft Copilot Studio.|A client name, which must be unique on the instance, and optionally a redirect URL.|[Add an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-an-mcp-client.md)|

To change a registered client, select its name, or select **Edit** from the actions menu on its row. For details, see [Edit a registered client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/edit-a-registered-client.md). To remove a client, select **Delete** from the actions menu on its row, and then select **Delete** in the confirmation dialog. You can't undo a deletion. For an overview of client registration, see [Client registration and AI Gateway setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/client-registration.md).

When access management is on for the server, a registered client is authorized to use only the tools that its client access policies grant through AI Gateway. For details, see [Controlling which tools clients can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md).

## Connect the agent

How you connect an agent depends on where the agent runs and how the MCP server was registered:

|If|Then|Details|
|---|----|-------|
|An AI Agent Studio agent already uses the MCP server directly|Update the agent's MCP server tool to use the AI Gateway connection details and the client's credentials.|[Register via AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-register-mcp-servers-via-ai-agent-studio.md)|
|The MCP server was added in AI Control Tower, and the agent runs in AI Agent Studio|Register the server in AI Agent Studio, and then add it to the agent as a tool.|[Register an MCP server via AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-add-a-new-mcp-server-to-an-agent.md)|
|The agent runs on an external platform, such as Microsoft Copilot Studio, Google Gemini, or Amazon Bedrock|Set the AI Gateway MCP server URL as the agent's MCP server endpoint, and use the registered client's credentials. For the steps, see the platform's documentation.|[Configure agents to use MCP servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configure-agents-to-use-mcp-servers.md)|

## Connection details

The **AI Gateway MCP server details** panel on the **Setup** sub-tab shows the details that agents use. The same panel also appears on the record's **Overview** tab. If the server has more than one variant, the panel shows the details for the variant selected in the **CIMD and MCP client integration** panel. Select the copy icon next to a URL to copy it.

|Field|Description|
|-----|-----------|
|AI Gateway MCP server URL|The URL that agents call instead of the MCP server's own URL, for example `https://<instance>.service-now.com/sncapps/awh/<mcp-server>/mcp`.|
|Authorization endpoint URL|The OAuth authorization endpoint, `https://<instance>.service-now.com/mcp_auth.do`.|
|Token endpoint URL|The OAuth token endpoint, `https://<instance>.service-now.com/mcp_token.do`.|

