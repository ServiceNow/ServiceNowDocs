---
title: MCP connections and Build Agent
description: MCP connections enable Build Agent to access external tools and resources through standardized communication. Use these connections to integrate third-party applications like Figma for accelerated design-to-development workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/accelerate-design-to-development-with-figma-mcp-server.html
release: australia
topic_type: concept
last_updated: "2026-10-20"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# MCP connections and Build Agent

MCP connections enable Build Agent to access external tools and resources through standardized communication. Use these connections to integrate third-party applications like Figma for accelerated design-to-development workflows.

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

You can create custom MCP servers on the ServiceNow AI Platform and then have Build Agent connect to them. For information about creating custom MCP servers, see [Create a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-mcp-server.md).

MCP is an open protocol that defines how AI agents communicate with external systems to discover and invoke tools, retrieve resources, and share context. By standardizing this communication layer, MCP enables AI agents to interact with a wide range of third-party applications without requiring custom integration logic for each one.

In Connect Hub, an MCP connector represents a configured connection between ServiceNow and an external system that exposes a server compatible with MCP. After you set up an MCP connector, AI agents can use it to access tools and capabilities from the external system, enabling coordinated workflows across models and systems.

## Configuration details

For details on configuring MCP connections in Build Agent, see [Connect Build Agent to a supported MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ba-connct-mcp-server.md). For more information on MCP connections, see [Additional connector configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/additional-configs-mcr.md).

## Connect to supported MCP servers

Build Agent can use any MCP connection that's available in an instance's registry, though you must manually authenticate the connection the first time you use it with Build Agent.

For details on adding a new MCP connection in Workflow Data Fabric, see [Model Context Protocol connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/model-context-protocol-connector.md).

An example prompt: `Let's create a new project to track my baby's sleep and create issues in Linear based on inputs from the tracker`.

**Note:** MCP connections are available in both ServiceNow Studio and the ServiceNow IDE.

## Approve and activate MCP servers

Before you can enable an MCP server in Build Agent, a user with the sn\_ai\_governance.ai\_steward role must approve it as an AI asset in AI Control Tower. An administrator without this role can't approve the server. Each MCP server requires this approval, regardless of whether the server is enabled by default. For the approval steps, see [Onboard MCP server approval playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-onboard-mcp-server-approval-playbook.md).

The end-to-end flow for making an MCP server available is:

1.  The administrator adds the MCP server as a Workflow Data Fabric \(WDF\) connection.
2.  A user with the sn\_ai\_governance.ai\_steward role approves the server as an AI asset in AI Control Tower.
3.  You authenticate the connection in Personal Integrations.For details, see [Using the Personal Authentication dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/personal-auth-dashboard.md).
4.  You enable the MCP server in Build Agent settings.

For details on adding the MCP server connection, see the following topics:

-   [Dynamic client registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mcp-dcr-a.md) for servers that connect with one click
-   [Manual client registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mcp-mcr-a.md) for servers marked **Manual setup may be required**
-   [Client registration using custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mcp-custom.md) for servers that aren't in the MCP registry

Individual MCP servers are enabled by default, but the complete flow must be completed before any server is available for use.

For details on adding a new MCP connection in Workflow Data Fabric, see [Model Context Protocol connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/model-context-protocol-connector.md).

## View available tools per MCP server

You can view the list of tools available for each connected MCP server in the **MCP servers** pane in the Build Agent settings panel. Expand a server by selecting the chevron next to the server name to see its tools and descriptions.

\[Omitted image "ba-mcp-list-tools.png"\] Alt text: MCP Servers panel listing enabled servers with Zoom Chat expanded to show available tools and descriptions.

## Application development with Figma MCP server

Connect the Figma MCP server to the Build Agent to accelerate the transition of your Figma designs to applications on the ServiceNow AI Platform®.

**Note:** You can upload additional types of files to accelerate development, such as images and code files. For more information, see [Supported file types for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ba-supported-file-types.md).

The Figma MCP \(Model Context Protocol\) server establishes a secure connection between the Build Agent and Figma using OAuth for login authentication. This server enables the Build Agent to access structured design data directly from Figma files, instead of using static screen captures. With the available data, the Build Agent can generate applications.

The Figma MCP server translates Figma data, such as components, styles, and variables, into a machine-readable format. The Build Agent uses the translated data to generate code, gather design context, or develop design systems directly from Figma. Developers can create more accurate and consistent application UIs \(user interfaces\).

The process of converting Figma designs to applications is as follows:

-   Designers use Figma to create UI components, styles, and variables.
-   The Figma MCP server uses OAuth to securely access design data from Figma.
-   The Figma MCP server acts as an intermediary, converting Figma design data into the Build Agent context.
-   The Build Agent, which is installed on your ServiceNow® instance, receives the translated data and uses it to generate applications.
-   The Build Agent creates applications based on the design data provided by Figma.

**Note:** An allowlist process is required to connect the Build Agent MCP client to the Figma MCP server. Contact Now Support to initiate the process.

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/exploring-build-agent.md)

