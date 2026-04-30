---
title: Exploring MCP Server Console
description: Learn about how you can use Model Context Protocol \(MCP\) servers to allow AI applications to access data and perform actions on a ServiceNow instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 4
keywords: [explore]
breadcrumb: [MCP Server Console, Enable AI experiences]
---

# Exploring MCP Server Console

Learn about how you can use Model Context Protocol \(MCP\) servers to allow AI applications to access data and perform actions on a ServiceNow instance.

## MCP Server Console overview

The Model Context Protocol defines a standard method of communication between large language models \(LLMs\) and external systems, such as a ServiceNow instance. AI applications connect to an external system from an MCP client, such as an AI agent, using an MCP server. The server tells the client which external resources it can access and how to access them. Then, from an MCP client, users can request information from the server and automate functionality using the available tools and data that the server returns. For general information about the Model Context Protocol and MCP terminology, see the [Model Context Protocol documentation](https://modelcontextprotocol.io/docs/learn/server-concepts) on the modelcontextprotocol.io website.

With MCP Server Console, you can create MCP servers on an instance and configure the tools that they expose or use a preconfigured Quickstart Server. Tools define which functionality and data a server exposes to clients and the actions that can be performed on an instance by clients. You can create tools based on existing capabilities, such as Now Assist skills.

Then any AI application, such as Microsoft Copilot or Claude, can call a server from a client using OAuth 2.0 authentication and get a list of available tools. With these tools, employees using MCP clients can prompt the server for information from the instance or to perform an action on the instance, such as to summarize a list of recently closed incidents or cases. You can also use the ServiceNow Model Context Protocol Client to let an AI application on one instance access tools from an MCP server on another instance.

## MCP Server Console users

|User|Description|
|----|-----------|
|AI administrator|AI administrators can create MCP servers and configure which tools they expose to MCP clients. They also create OAuth inbound integrations on the instance for each client and configure clients with the server and authentication details.|

## MCP Server Console workflow

The following infographic shows the workflow for AI administrators to get started managing MCP servers with MCP Server Console.

![Process for managing MCP servers on a ServiceNow instance and connecting to a server from an MCP client in an AI application. For details, refer to the following description.](../image/mcp-server-console-workflow.svg "Managing MCP servers with MCP Server Console")

1.  As an AI administrator, you identify which functionality on an instance to access from an external MCP client and employee experience.
2.  You can use the preconfigured Quickstart Server or create an MCP server with the appropriate tools to use the desired functionality.

    You can create one or more servers that expose different tools for different use cases, such as for HR or IT workflows, or for different clients.

3.  If needed, you can create additional tools from Now Assist skills and configure which fields are exposed to clients and then add the tools to servers.
4.  You create OAuth inbound integrations for each client to secure access to servers on an instance.
5.  You configure clients to connect to a server using the server and OAuth inbound integration details.

    Then the client calls the server, which validates the OAuth token and responds with the list of tools available for use with the server.

6.  Employees use clients, such as AI agents, to prompt the server for data from the instance or to perform an action on the instance.

**Note:** With AI Gateway in AI Control Tower, AI administrators can monitor MCP server access and view metrics for servers and their tools. For more information, see [AI Gateway](../../ai-governance-workspace/concept/ai-gateway-overview.md).

## MCP Server Console benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Integrate with any AI application and MCP client using a standard protocol.|[Create a Model Context Protocol server](../task/create-mcp-server.md)|AI administrator|
|Control which tools and fields are exposed to MCP clients.|[Create a tool for a Model Context Protocol server](../task/create-tool-mcp-server.md)|AI administrator|
|Securely access functionality from a ServiceNow instance in any external employee experience.|[Configure an MCP client to connect to an MCP server](connect-mcp-server-client.md#)|AI administrator|

## Quickstart Server in MCP Server Console

MCP Server Console includes a preconfigured Quickstart Server to help you get started learning about MCP servers and connecting MCP clients to a ServiceNow instance. The Quickstart Server includes tools for looking up and summarizing incident and case records.

|Name|Description|
|----|-----------|
|Case summarization|Get a summary of details in a case record generated by Now Assist.|
|Incident summarization|Get a summary of details in an incident record generated by Now Assist.|
|Look up Case Records|Look up case records to enable summarizing them with the Case Summarization tool.|
|Look up Incident Records|Look up incident records to enable summarizing them with Incident summarization tool.|

## What to explore next

To learn more about configuring and using MCP Server Console, see:

-   [Configuring MCP Server Console](configuring-mcp-server-console.md)
-   [Configure an MCP client to connect to an MCP server](connect-mcp-server-client.md#)
-   [MCP Server Console reference](mcp-server-console-reference.md)

**Related topics**  


[Model Context Protocol Client](../../model-context-protocol-client/reference/mcp-client.md)

