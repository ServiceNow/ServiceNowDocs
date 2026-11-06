---
title: Connect Build Agent to a supported MCP server
description: Connect a supported MCP server to Build Agent to access external tools and resources in the chat panel when building and editing apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/ba-connct-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-10-29"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Connect Build Agent to a supported MCP server

Connect a supported MCP server to Build Agent to access external tools and resources in the chat panel when building and editing apps.

## Before you begin

Before you can enable an MCP server in Build Agent, a user with the sn\_ai\_governance.ai\_steward role must approve it as an AI asset in AI Control Tower. An administrator without this role can't approve the server. Each MCP server requires this approval, regardless of whether the server is enabled by default. For the approval steps, see [Onboard MCP server approval playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-onboard-mcp-server-approval-playbook.md).

You must have Connect Hub installed.

**Note:** MCP settings currently apply to Build Agent, not Autonomous Engineer.

The end-to-end flow for making an MCP server available is:

1.  The administrator adds the MCP server as a Workflow Data Fabric \(WDF\) connection.
2.  A user with the sn\_ai\_governance.ai\_steward role approves the server as an AI asset in AI Control Tower.
3.  You authenticate the connection in Personal Integrations.For details, see [Using the Personal Authentication dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/personal-auth-dashboard.md).
4.  You enable the MCP server in Build Agent settings.

For details on adding the MCP server connection, see the following topics:

-   [Dynamic client registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mcp-dcr-a.md) for servers that connect with one click
-   [Manual client registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mcp-mcr-a.md) for servers marked **Manual setup may be required**
-   [Client registration using custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mcp-custom.md) for servers that aren't in the MCP registry

**Note:** An allowlist process is required to connect the Build Agent MCP client to the Figma MCP server. Contact Now Support to initiate the process.

Individual MCP servers are enabled by default, but the complete flow must be completed before any server is available for use.

For details on adding a new MCP connection in Workflow Data Fabric, see [Model Context Protocol connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/model-context-protocol-connector.md).

See [MCP connections and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/accelerate-design-to-development-with-figma-mcp-server.md) for a list of supported MCP servers.

**Note:** MCP connections are available in both ServiceNow Studio and the ServiceNow IDE.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

2.  Select the Conversations icon \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text: in the Navigator panel to open Build Agent.

3.  Select the Settings icon \[Omitted image "ba-settings-icon.png"\] Alt text: in the Build Agent chat panel.

    \[Omitted image "ba-settings-panel-1.png"\] Alt text: Build Agent panel showing greeting message and the Settings button

4.  Select the **Enable MCP servers** toggle on the **MCP** tab.

5.  Select the MCP server to enable.

    \[Omitted image "ba-settings-panel-mcp-tab.png"\] Alt text: MCP tab of the Settings panel with the Enable MCP servers and ATF Cloud runner toggles turned on.

    **Note:** If the MCP server isn't available, authenticate the connection first. Navigate to **All** &gt; **IntegrationHub** &gt; **Personal Authentication** &gt; **Personal Integrations**. This task requires the sn\_personal\_auth.personal\_auth\_user role. For more information, see [Using the Personal Authentication dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/personal-auth-dashboard.md).

6.  Select **Allow** in the confirmation dialog.

    You must do this only for the initial connection.

7.  View the list of available tools that you can call for each MCP server by expanding the server name.

    \[Omitted image "ba-mcp-list-tools.png"\] Alt text: MCP Servers panel showing available tools.


## Result

After Build Agent authenticates the connection, you can chat with it to ask questions related to the MCP server.

**Parent Topic:**[Build Agent configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-build-agent.md)

