---
title: Connect the EA MCP server to an AI assistant
description: After configuring the EA MCP server, connect it to an AI assistant so the assistant can query business applications, capabilities, and architectural insights directly from your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/connect-ea-mcp-server-to-ai-assistant.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [MCP server, AI assistant, EA MCP, connect MCP]
breadcrumb: [Configure MCP, MCP for Enterprise Architecture, Enterprise Architecture]
---

# Connect the EA MCP server to an AI assistant

After configuring the EA MCP server, connect it to an AI assistant so the assistant can query business applications, capabilities, and architectural insights directly from your ServiceNow instance.

## Before you begin

-   The MCP for Enterprise Architecture application is installed. For details, see [Install MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/install-mcp-for-ea.md).
-   Confirm that the EA MCP server is active on your instance by navigating to **All** &gt; **MCP Server Console**. If you don't see the server or to create another MCP server, see [Create a Model Context Protocol server](https://www.servicenow.com/docs/r/intelligent-experiences/create-mcp-server.html?content-lang=en-US)

    \[Omitted image "mcp-for-ea-active-state.png"\] Alt text: MCP Server Console showing the EA MCP Server card with an Active status indicator.

-   Confirm that the MCP for EA tools are enabled on your instance by navigating to **All** &gt; **MCP Server Console** &gt; **Tools**. To see which operations a tool can perform, open the tool and view its **Annotations** field. For example, the readOnlyHint annotation indicates that the tool only retrieves data.

    \[Omitted image "mcp-for-ea-tools-status.png"\] Alt text: Tools list in MCP Server Console with the Active column highlighted, showing EA MCP tools set to true.


Role required: admin or sn\_mcp\_server.admin

## Procedure

1.  Connect the EA MCP server to your AI assistant.

    For instructions, see [Connecting to an MCP server from an MCP client](https://www.servicenow.com/docs/r/intelligent-experiences/connect-mcp-server-client.html?content-lang=en-US).

    Use the following values when configuring the connection:

    -   **Server URL:** `https://*instance*.service-now.com/sncapps/mcp-server/mcp/sn_ea_mcp_server_ea_mcp_server`, where *instance* is your ServiceNow instance name.
    -   **Connection method:** `npx mcp-remote` with Bearer token authentication.
    **Note:** If you're using Claude Desktop, add an entry with the key `sn-gen-ai-ea` to your MCP server configuration file and set the `command` to `npx`.


**Parent Topic:**[Configure MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/configuring-ea-mcp-server.md)

**Related topics**  


[Enable Knowledge Graph system properties for the Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/set-kg-system-properties-ea-qna.md)

[Configure ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/configure-now-assist-ea.md)

[Enterprise Architecture Workspace access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-access-roles.md)

