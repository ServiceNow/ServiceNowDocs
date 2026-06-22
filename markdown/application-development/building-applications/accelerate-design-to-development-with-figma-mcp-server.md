---
title: MCP connections and Build Agent
description: MCP connections enable Build Agent to access external tools and resources through standardized communication. Use these connections to integrate third-party applications like Figma for accelerated design-to-development workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/accelerate-design-to-development-with-figma-mcp-server.html
release: australia
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# MCP connections and Build Agent

MCP connections enable Build Agent to access external tools and resources through standardized communication. Use these connections to integrate third-party applications like Figma for accelerated design-to-development workflows.

The following MCP connections are currently supported for Build Agent:

-   Atlassian Rovo
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

MCP is an open protocol that defines how AI agents communicate with external systems to discover and invoke tools, retrieve resources, and share context. By standardizing this communication layer, MCP allows AI agents to interact with a wide range of third-party applications without requiring custom integration logic for each one.

In Connect Hub, an MCP connector represents a configured connection between ServiceNow and an external system that exposes a server compatible with MCP. Once an MCP connector is set up, AI agents can use it to access the tools and capabilities that the external system provides, enabling coordinated, context-aware workflows across models and systems.

For details on configuring MCP connections in Build Agent, see [Connect Build Agent to a supported MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/ba-connct-mcp-server.md). For more information on MCP connections, see [Additional connector configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/additional-configs-mcr.md).

## Connect to supported MCP servers

Build Agent can use any MCP connection that's available in an instance's registry, though you must manually authenticate the connection the first time you want to use it with Build Agent.

For details on adding a new MCP connection in Workflow Data Fabric, see [Model Context Protocol connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/model-context-protocol-connector.md).

An example prompt could be something like the following: `Let's create a new project to track my baby's sleep and create issues in Linear based on inputs from the tracker`.

**Note:** MCP connections are available in both ServiceNow Studio and the ServiceNow IDE, though you must be on Australia Patch 3 or higher to use MPC servers with Build Agent in ServiceNow Studio.

## Approve and activate MCP servers

Before you can enable an MCP server in Build Agent, an administrator must approve it as an AI asset in AI Control Tower. Each MCP server requires this approval, regardless of whether the server is enabled by default.

The end-to-end flow for making an MCP server available is:

1.  The administrator adds the MCP server as a Workflow Data Fabric \(WDF\) connection.
2.  The administrator approves the server as an AI asset in AI Control Tower.
3.  You authenticate the connection in Personal Integrations.
4.  You enable the MCP server in Build Agent settings.

Individual MCP servers are enabled by default, but the complete flow must be completed before any server is available for use.

For details on adding a new MCP connection in Workflow Data Fabric, see [Model Context Protocol connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/model-context-protocol-connector.md).

## Application development with Figma MCP server

Connect the Figma MCP server to the Build Agent to accelerate the transition of your Figma designs to enterprise-grade applications on the ServiceNow AI Platform®.

**Note:** You can upload additional types of files to accelerate development, such as images and code files. For more information, see [Supported file types for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/ba-supported-file-types.md).

The Figma MCP \(Model Context Protocol\) server establishes a secure connection between the Build Agent and Figma using OAuth for login authentication. This server enables the Build Agent to access structured design data directly from Figma files, rather than relying on static screen captures. With the available data, the Build Agent can effectively create applications.

The Figma MCP server translates Figma data, such as components, styles, and variables, into a machine-readable format. The Build Agent uses the translated data to generate code, gather design context, or develop design systems directly from Figma. Consequently, developers can create more accurate and consistent application UIs faster than with traditional approaches.

The process of converting Figma designs to applications is as follows:

-   Designers use Figma to create user interface \(UI\) components, styles, and variables.
-   The Figma MCP server employs OAuth to securely access design data from Figma.
-   The Figma MCP server acts as an intermediary, converting Figma’s design data into the Build Agent context.
-   The Build Agent, which is installed on your ServiceNow® instance, receives the translated data and uses it to generate applications.
-   The Build Agent creates applications based on the design data provided by Figma.

For configuration information, see [Connect Build Agent to a Figma MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/connect-figma-mcp-server-to-build-agent.md).

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/exploring-build-agent.md)

