---
title: Configure an AI agent as an MCP tool
description: Enable an AI agent to be discoverable and accessible as an MCP tool by configuring authentication, communication mode, and third-party access settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/configure-ai-agent-as-mcp-tool.html
release: zurich
topic_type: task
last_updated: "2026-09-21"
reading_time_minutes: 1
keywords: [AI agent, MCP tool, configuration, authentication]
breadcrumb: [Activate the ITSM MCP Server, ITSM MCP Server, IT Service Management]
---

# Configure an AI agent as an MCP tool

Enable an AI agent to be discoverable and accessible as an MCP tool by configuring authentication, communication mode, and third-party access settings.

## Before you begin

You must have access to AI Agent Studio and permission to configure authentication settings.

Role required: admin

## Procedure

1.  Navigate to the MCP server authentication configuration and activate the ITSM MCP server.

    In the authentication scope field, select **A2A auth scope**. This enables the REST A2A protocol to access your AI agent MCP tools. For information on activating the ITSM MCP Server, see [Activate the ITSM MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/set-up-itsm-mcp-server.md).

2.  Configure the communication mode for external AI agents in AI Agent Studio.

    1.  Navigate to **AI Agent Studio** &gt; **Settings**.

    2.  In the left panel, select **Discoverability**.

    3.  Enable the communication mode options and set the communication mode to **Synchronous**.

3.  Enable third-party access on the AI agent definition.

    In AI Agent Studio, open the AI agent and navigate to the **Define the specialty** screen. Enable the toggle for **Allow third party access to this AI agent**.

    **Note:** To make modifications to the record such as allowing third party to access the AI agent, see [Duplicate an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/clone-ai-agent.md). You must also update the agent sys\_id in the corresponding tool input of the MCP tool.

    \[Omitted image "itsm-mcp-server-allow-third-party-access.png"\] Alt text: Allow third party to access this AI agent toggle set to enabled.


## What to do next

After completing these steps, the AI agent is discoverable as an MCP tool and can be used by external systems and workflows.

**Related topics**  


[Configure an MCP client to connect to an MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-client-connect-server.md)

