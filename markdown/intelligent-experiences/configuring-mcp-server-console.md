---
title: Configuring MCP Server Console
description: Create a Model Context Protocol \(MCP\) server and configure the tools and inputs it exposes to MCP clients.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [MCP Server Console, Enable AI experiences]
---

# Configuring MCP Server Console

Create a Model Context Protocol \(MCP\) server and configure the tools and inputs it exposes to MCP clients.

## Configuration overview

1.  [Create a Model Context Protocol server](../task/create-mcp-server.md)

    An AI administrator creates a server and adds tools to the server.

2.  [Create a tool for a Model Context Protocol server](../task/create-tool-mcp-server.md)

    If additional tools are needed, the AI administrator identifies which functionality to expose and creates tools based on Now Assist skills. From the tools, they configure which fields are exposed to clients as tool inputs.


After configuring a server, the AI administrator creates an OAuth inbound integration for each client and configures clients to connect to the server using the server and authentication details. For more information, see [Connecting to an MCP server from an MCP client](connect-mcp-server-client.md#).

