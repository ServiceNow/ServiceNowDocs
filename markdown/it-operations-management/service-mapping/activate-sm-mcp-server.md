---
title: Activate the Now Assist CMDB MCP Server for Service Mapping tools
description: Activate the Now Assist CMDB MCP Server and configure the OAuth inbound integration so that external AI clients can connect to your ServiceNow instance and query application service data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-mapping/activate-sm-mcp-server.html
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 3
keywords: [MCP Server, Service Mapping, activate, OAuth, MCP Server Console, Machine Identity Console]
breadcrumb: [Service Mapping MCP tools, AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Activate the Now Assist CMDB MCP Server for Service Mapping tools

Activate the Now Assist CMDB MCP Server and configure the OAuth inbound integration so that external AI clients can connect to your ServiceNow® instance and query application service data.

## Before you begin

Before activating the Now Assist CMDB MCP Server, confirm the following requirements are met.

-   Verify that Zurich Patch 10 is installed.
-   You have the MCP Platform Manager version 1.4.0 \(or later\) plugin activated.
-   You have the Now Assist CMDB MCP Server \(sn\_cmdb\_gen\_ai.now\_assist\_cmdb\_mcp\_server\) application installed.
-   You have the roles required as described in [Configure roles for the Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-config-role-hierarchy.md).

Role required: admin assigned with the sn\_mcp\_server.admin role, and the oauth\_admin \(or mi\_admin\) role

\[Omitted image "sm-mcp-roles.png"\] Alt text: service\_mapping\_user contains sn\_sm\_gen\_ai.sm\_mcp\_user, which contains sn\_mcp\_server.viewer. The sn\_sm\_gen\_ai.sm\_mcp\_admin role separately contains sn\_sm\_gen\_ai.sm\_mcp\_user.

## About this task

The Service Mapping MCP tools are delivered as part of the Now Assist CMDB MCP Server \(sn\_cmdb\_gen\_ai.now\_assist\_cmdb\_mcp\_server\). Activating it exposes five read-only tools that AI clients can use to query live application service data. The OAuth inbound integration for this server is auto-generated when the server is installed. You must locate this integration, verify its configuration, and add the redirect URL for the AI client before users can authenticate.

For detailed information, see [Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-mcp-server.md)

## Procedure

1.  On your ServiceNow instance, navigate to **All** &gt; **MCP Server Console**.

2.  From the **Configuration** tab, select **Servers**.

3.  Select the **Now Assist CMDB MCP Server** tile.

    **Note:** If the server does not appear, change the application scope to **ITOM AI Agents for Service Mapping**. The MCP Server Console screen opens with all fields populated, including the server URL and short description.

4.  From the **Deactivate** menu, select **Activate**.

    The server status is set to **Active**. The individual tools are active by default. \[Omitted image "sm-mcp-active.png"\] Alt text: The Active indication

5.  Configure the OAuth inbound integration so that AI clients can authenticate with your instance.

    **Important:** Do not create a new OAuth client for this integration. The integration named sn\_cmdb\_gen\_ai.now\_assist\_cmdb\_mcp\_server is auto-generated when the server is installed. Creating a custom client requires manual auth scope configuration, and misconfiguration is silent — the connection succeeds but no tools appear in the AI client.

    1.  Set the scope to **Global**.

    2.  Navigate to **All** &gt; **Machine Identity Console** and select the **Inbound integrations** tab.

    3.  Locate and open the integration named **sn\_cmdb\_gen\_ai.now\_assist\_cmdb\_mcp\_server**.

        **Note:** The inbound integrations list may also contain integrations whose names match other server names, including underscores. These are monitoring integrations created by AI Control Tower and should not be used for client connections.

    4.  Verify that the **Auth scope** field is set to **service\_mapping\_mcp\_auth\_scope**, limited to **MCP Tools API** and **CMDB Mcp Api**.

        **Important:** The auth scope must be service\_mapping\_mcp\_auth\_scope. Using a different scope, such as useraccount, results in a successful OAuth connection but no tools appear in the AI client.

    5.  In the **Redirect URLs** field, add the redirect URL for the AI client.

        For Claude Desktop, use: `https://claude.ai/api/mcp/auth_callback`.

    6.  Select **Save**.

6.  Note the **Client ID** and **Client Secret** displayed on the integration record, and provide them to users along with the server URL so they can configure their AI client connections.

    The server URL follows this format: `https://<instance>.service-now.com/sncapps/mcp-server/mcp/sn_cmdb_gen_ai_now_assist_cmdb_mcp_server`


## Result

The Now Assist CMDB MCP Server is active and the OAuth inbound integration is configured. Users can connect an AI client and authenticate using the Client ID, Client Secret, and server URL.

## What to do next

Share the following details with users so they can connect their AI clients: the server URL, the OAuth Client ID, and the OAuth Client Secret. For instructions on connecting Claude Desktop, see [Connect Claude Desktop to the Service Mapping MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/connect-claude-desktop-sm-mcp.md).

**Parent Topic:**[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-mcp-server.md)

