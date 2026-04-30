---
title: Adding an MCP Server in AI Agent Studio
description: An MCP Server hosts APIs and tools required by an AI application, allowing it to receive and process calls from MCP Clients to govern ingress traffic and to ensure secure and efficient access to tools. Adding an MCP Server in the AI Agent Studio helps you to leverage the Model Context Protocol as a tool in an AI agent.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Configuring Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Adding an MCP Server in AI Agent Studio

An MCP Server hosts APIs and tools required by an AI application, allowing it to receive and process calls from MCP Clients to govern ingress traffic and to ensure secure and efficient access to tools. Adding an MCP Server in the AI Agent Studio helps you to leverage the Model Context Protocol as a tool in an AI agent.

Connecting an MCP Server with the AI Agent Studio simplifies the integration process, making it easier to discover and invoke services. This connection enhances security and governance, providing a streamlined setup experience for administrators.

Adding an MCP Server requires you to add an MCP Server in the AI Agent Studio. You can add an MCP Server with one of the following authentication options:

1.  **OAuth 2.1**: Helps add an MCP Server with an authentication code. For more information, see [Add an MCP Server with OAuth 2.1](../task/add-an-oauth-2-1-mcp-server.md).

    **Note:** You can configure an MID Server to connect with MCP Client by adding it as an MCP server through OAuth 2.1 configuration and selecting the **Use MID server** check box on the respective server's Connection and Credentials Aliases record. For more information about connecting MCP Client with an MID Server through Connection and Credentials Aliases, see [Set up OAuth integration via MID Server](https://www.servicenow.com/docs/access?context=create-conn-alias-oauth-integration-via-mid-server&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

2.  **API Key**: Helps add an MCP Server with an API Key. For more information, see [Add an MCP Server with API Key](../task/add-an-api-key-mcp-server.md).
3.  **Others**: Helps add an MCP Server in a manual way by selecting a Connection and Credential Alias record. For more information, see [Add an MCP Server with Connection and Credential Alias](../task/add-an-mcp-server-with-connection-and-credential-alias.md).

