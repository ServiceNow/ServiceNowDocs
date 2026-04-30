---
title: Add an MCP server in AI Agent Studio
description: An MCP server hosts the APIs and tools required by an AI application to receive and process calls from MCP clients. The MCP server governs ingress traffic and promotes secure and efficient access to tools. Adding an MCP server in the AI Agent Studio helps you to leverage the Model Context Protocol as a tool for an AI agent.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Configure Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Add an MCP server in AI Agent Studio

An MCP server hosts the APIs and tools required by an AI application to receive and process calls from MCP clients. The MCP server governs ingress traffic and promotes secure and efficient access to tools. Adding an MCP server in the AI Agent Studio helps you to leverage the Model Context Protocol as a tool for an AI agent.

Connecting an MCP server with the AI Agent Studio simplifies the integration process, making it easier to discover and invoke services. This connection enhances security and governance, providing a streamlined setup experience for administrators.

**Note:** To connect MCP servers with AI Agent Studio, you must have installed the Now Assist AI Agents plugin \[sn\_aia\] as a prerequisite.

Adding an MCP server requires you to add an MCP server in the AI Agent Studio. You can add an MCPserver with one of the following authentication options:

-   **OAuth 2.1**: Add an MCP server with an authentication code. For more information, see [Add an MCP server with OAuth 2.1](../task/add-an-oauth-2-1-mcp-server.md).

    **Note:** You can configure an MID Server to connect with MCP Client by adding it as an MCP server through OAuth 2.1 configuration and selecting the **Use MID server** check box on the respective server's Connection and Credentials Aliases record. For more information about connecting MCP Client with an MID Server through Connection and Credentials Aliases, see [Set up OAuth integration via MID Server](https://www.servicenow.com/docs/access?context=create-conn-alias-oauth-integration-via-mid-server&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

-   **API Key**: Add an MCP server with an API Key.
-   **Others**: Add an MCP server manually by selecting a Connection and Credential Alias record.

**Note:** You must authenticate the users with the MCP server to add the MCP tool to an AI agent. Without prior authentication, you can’t add the MCP servers.

