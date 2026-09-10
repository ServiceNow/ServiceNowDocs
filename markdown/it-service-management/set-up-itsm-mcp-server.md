---
title: Activate the ITSM MCP Server
description: Activate the ITSM MCP Server to enable AI-driven incident management, change management, or employee experience on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/set-up-itsm-mcp-server.html
release: zurich
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 1
keywords: [MCP Server, ITSM, Integration, OAuth, Incident Management, change management, AI integration, Model Context Protocol]
breadcrumb: [ITSM MCP Server, IT Service Management]
---

# Activate the ITSM MCP Server

Activate the ITSM MCP Server to enable AI-driven incident management, change management, or employee experience on your ServiceNow instance.

## About this task

## Before you begin

The following plugins must be activated on your instance:

-   ServiceNow Otto for IT Service Management \(ITSM\) plugin \(sn\_itsm\_gen\_ai\)
-   Model Context Protocol Server \(sn\_mcp\_server\)
-   ITSM MCP Server \(sn\_itsm\_mcp\_server\)

Role required: sn\_mcp\_server.admin or admin

## Procedure

1.  Activate the ITSM MCP Server.

    1.  Navigate to **All** &gt; **MCP Server Console**.

    2.  From the **Configuration** tab, select **Servers**.

    3.  Select the **ITSM MCP Server**.

        **Note:** Change the application scope to **ITSM MCP Server**.

        The **MCP Server Console** page opens with all fields populated by default.

        \[Omitted image "image.itsm-mcp-server-console"\] Alt text: ITSM MCP server Oauth access

    4.  In the **Auth scope** field, select **a2aauthscope**.

        Selecting this option enables the REST A2A protocol to access the AI Agent MCP tools.

    5.  From the **Deactivate** list, select **Activate**.

        **Note:**

        -   An OAuth client entry is created with the ITSM MCP Server integration name, for example, **sn\_itsm\_mcp\_server.itsm\_default**, which you can use to connect to the ITSM MCP Server using OAuth.
        -   The ITSM MCP Server is inactive by default. Activating the server automatically makes all registered tools available to connected MCP clients.
2.  Set up OAuth to securely authenticate the ITSM MCP Server with your ServiceNow instance.

    **Note:**

    -   If you use the ITSM MCP Server OAuth client entry to set up your OAuth server, the fields on the Authorization code grant page are automatically populated. Use this information to connect to the ITSM MCP Server.

        \[Omitted image "image.itsm-mcp-server-setup-oauth"\] Alt text: OAuth authorization code grant configuration form in Machine Identity Console showing fields for Name, Provider name, Redirect URLs, Client ID, and Client secret.

    -   If you're setting up your own OAuth connection, the oauth\_admin or admin role is required to configure your OAuth client entry. See the [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/connect-mcp-server-client.md) to set up the OAuth and connect to the ITSM MCP Server.

**Related topics**  


[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-mcp-server-console.md)

[Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/connect-mcp-server-client.md)

[Install Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-mcp-client.md)

