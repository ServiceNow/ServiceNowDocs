---
title: Activate the ITSM MCP Server
description: Activate the ITSM MCP Server to enable AI-driven incident management capabilities on your ServiceNow instance through Model Context Protocol \(MCP\) connectivity.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-04-16"
reading_time_minutes: 1
keywords: [MCP Server, ITSM, Integration, OAuth, Incident Management, AI integration, Model Context Protocol]
breadcrumb: [Use the ITSM MCP Server, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Activate the ITSM MCP Server

Activate the ITSM MCP Server to enable AI-driven incident management capabilities on your ServiceNow instance through Model Context Protocol \(MCP\) connectivity.

## About this task

## Before you begin

Role required: sn\_mcp\_server.admin or admin

You must have the following plugins installed on your instance:

-   Now Assist for IT Service Management \(ITSM\) plugin \(sn\_itsm\_gen\_ai\)
-   Model Context Protocol Server \(sn\_mcp\_server\)

## Procedure

1.  Activate the ITSM MCP Server.

    1.  Navigate to **All** &gt; **MCP Server Console**.

    2.  From the Configuration tab, select **Servers**.

    3.  Select the **ITSM MCP Server**.

        **Note:** You must change the application scope to **ITSM MCP Server**.

        The **MCP Server Console** screen opens with all fields populated. ![ITSM MCP Server configuration details page](../image/now-assist-itsm-mcp-server-console.png)

    4.  From the Deactivate drop-down menu, select **Activate**.

        **Note:** An OAuth client entry is created with the ITSM MCP Server integration name, for example, **sn\_itsm\_mcp\_server.itsm\_default** that you can use to connect to the ITSM MCP Server using OAuth.

2.  Set up OAuth to securely authenticate the ITSM MCP Server with your ServiceNow instance.

    **Note:**

    -   If you are using the ITSM MCP Server OAuth client entry to set up your OAuth server, the fields in the Authorization code grant screen are filled in automatically and you will use this information to connect to the ITSM MCP Server.

        ![OAuth authorization code grant configuration form in Machine Identity Console showing fields for Name, Provider name, Redirect URLs, Client ID, and Client secret.](../image/now-assist-itsm-mcp-setup-oauth.png)

    -   If you're setting up your own OAuth connection, you need either an oauth\_admin, or admin role to configure your OAuth client entry. Refer to the instructions in the [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md) to setup the OAuth and connect to the ITSM MCP Server.

**Related topics**  


[MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mcp-platform-manager-landing.md)

[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-mcp-server-console.md)

[Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md)

[Install Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-mcp-client.md)

