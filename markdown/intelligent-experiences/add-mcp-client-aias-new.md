---
title: Adding an MCP Server Console in AI Agent Studio
description: An MCP Server Console hosts the APIs and tools required by an AI application. It receives and processes calls from MCP Clients to govern ingress traffic and promote secure access to tools. Adding an MCP Server Console in the AI Agent Studio helps you to leverage the Model Context Protocol as a tool in the ServiceNow agentic AI system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-mcp-client-aias-new.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Model Context Protocol Client, MCP Client, AI Agent Studio, Enable AI experiences]
---

# Adding an MCP Server Console in AI Agent Studio

An MCP Server Console hosts the APIs and tools required by an AI application. It receives and processes calls from MCP Clients to govern ingress traffic and promote secure access to tools. Adding an MCP Server Console in the AI Agent Studio helps you to leverage the Model Context Protocol as a tool in the ServiceNow agentic AI system.

Connecting an MCP Server Console with the AI Agent Studio simplifies the integration process, making it easier to discover and invoke services. This connection enhances security and governance, providing a streamlined setup experience for administrators.

Adding an MCP Server Console requires you to add an MCP Server Console in the AI Agent Studio. You can add an MCP Server Console with one of the following authentication options:

1.  **OAuth 2.1**: Helps add an MCP Server Console with an authentication code. For more information, see [Add an MCP server with OAuth 2.1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-an-oauth-2-1-mcp-server.md).
2.  **API Key**: Helps add an MCP Server Console with an API Key. For more information, see [Add an MCP Server with API Key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-an-api-key-mcp-server.md).
3.  **Others**: Helps add an MCP Server Console in a manual way by selecting a Connection and Credential Alias record. For more information, see [Add an MCP Server with Connection and Credential Alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-an-mcp-server-with-connection-and-credential-alias.md).

**Note:** You must authenticate the users with the MCP Server Console to add the MCP tool to an AI agent and without prior authentication, you can’t add the MCP Server Console.

