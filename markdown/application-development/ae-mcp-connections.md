---
title: MCP connections and Autonomous Engineer
description: MCP connections enable Autonomous Engineer to access external tools and resources through standardized communication, extending the planning and implementation workflow with data and context from third-party systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/ae-mcp-connections.html
release: australia
topic_type: concept
last_updated: "2026-09-23"
reading_time_minutes: 3
keywords: [Autonomous Engineer, MCP, Model Context Protocol, external tools, connections]
audience: programmer
breadcrumb: [Overview, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# MCP connections and Autonomous Engineer

MCP connections enable Autonomous Engineer to access external tools and resources through standardized communication, extending the planning and implementation workflow with data and context from third-party systems.

MCP is an open protocol that defines how AI agents communicate with external systems to discover and invoke tools, retrieve resources, and share context. By standardizing this communication layer, MCP enables AI agents to interact with a wide range of third-party applications without requiring custom integration logic for each one.

In Connect Hub, an MCP connector represents a configured connection between ServiceNow and an external system that exposes a server compatible with MCP. After an administrator sets up an MCP connector and you authenticate your connection, Autonomous Engineer can use it to access tools and capabilities from the external system. This enables Autonomous Engineer to pull in external context during planning and to create records in connected systems as part of implementation.

## How Autonomous Engineer uses MCP connections

Autonomous Engineer and Build Agent share the same MCP connection registry. Connections that are approved, authenticated, and enabled for Build Agent are available to Autonomous Engineer in the same session. You don't have to configure connections separately for each product.

Autonomous Engineer can use MCP connections at any stage of the workflow. For example, during planning, Autonomous Engineer can read requirements from a connected project management tool. During implementation, it can create or update records in connected systems as part of executing a plan.

## Approve and activate MCP servers

Before you can enable an MCP server in Build Agent, an administrator must approve it as an AI asset in AI Control Tower. Each MCP server requires this approval, regardless of whether the server is enabled by default.

The end-to-end flow for making an MCP server available is:

1.  The administrator adds the MCP server as a Workflow Data Fabric \(WDF\) connection.
2.  The administrator approves the server as an AI asset in AI Control Tower.
3.  You authenticate the connection in Personal Integrations.
4.  You enable the MCP server in Build Agent settings.

For details on enabling MCP connections, see [Client registration using custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mcp-custom.md).

Individual MCP servers are enabled by default, but the complete flow must be completed before any server is available for use.

For details on adding a new MCP connection in Workflow Data Fabric, see [Model Context Protocol connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/model-context-protocol-connector.md).

## Supported MCP servers

The following MCP connections are currently supported for Build Agent:

-   Atlassian Rovo
-   AWS DevOps
-   Box
-   Docusign
-   Figma
-   Linear
-   Miro
-   Prisma Postgres
-   Zoom
-   Zoom Chat
-   Zoom Docs
-   Zoom Whiteboard

**Note:** Because Build Agent doesn't support multiple servers connecting to one app, each Zoom integration requires its own app in Zoom.

## View available tools per MCP server

You can view the tools available for each connected MCP server in the **MCP servers** tab in the Build Agent settings panel. Expand a server by selecting the chevron next to the server name to see its tools and descriptions. Because Autonomous Engineer runs within the Build Agent interface, the same pane applies when Autonomous Engineer is the active mode.

## How to configure MCP connections

For details on configuring MCP connections, see [Connect Build Agent to a supported MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ba-connct-mcp-server.md). Because Autonomous Engineer shares the Build Agent settings panel, the configuration steps are the same for both products. For more information on MCP connections on the platform, see [Additional connector configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/additional-configs-mcr.md).

**Parent Topic:**[Exploring Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/exploring-autonomous-engineer.md)

