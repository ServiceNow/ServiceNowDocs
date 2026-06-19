---
title: Connect Claude Desktop to the Service Mapping MCP Server
description: Add the Service Mapping MCP Server as a custom connector in Claude Desktop so you can query application service data from your ServiceNow instance in natural language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-mapping/connect-claude-desktop-sm-mcp.html
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 3
keywords: [Claude Desktop, MCP Server, Service Mapping, connect, OAuth, ITOM, Now Assist, CMDB]
breadcrumb: [Service Mapping MCP tools, AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Connect Claude Desktop to the Service Mapping MCP Server

Add the Service Mapping MCP Server as a custom connector in Claude Desktop so you can query application service data from your ServiceNow® instance in natural language.

## Before you begin

Before connecting Claude Desktop to the Service Mapping MCP Server, confirm the following requirements are met.

-   Claude Desktop is installed on your computer.
-   You have a Claude account with permission to add custom MCP connectors. If your organization manages Claude through an Enterprise or Team plan, verify that custom connectors are enabled in your organization's settings.
-   The Service Mapping MCP Server is active, and you have the following details:

    -   MCP Server URL
    -   OAuth Client ID
    -   OAuth Client Secret
    For more information, see: [Activate the Now Assist CMDB MCP Server for Service Mapping tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/activate-sm-mcp-server.md)

-   Verify that you have the required role configuration. For more information, see [Configure roles for the Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-config-role-hierarchy.md).

    Role required: service\_mapping\_user assigned with the sn\_sm\_gen\_ai.sm\_mcp\_user role

    \[Omitted image "sm-mcp-roles.png"\] Alt text: service\_mapping\_user contains sn\_sm\_gen\_ai.sm\_mcp\_user, which contains sn\_mcp\_server.viewer. The sn\_sm\_gen\_ai.sm\_mcp\_admin role separately contains sn\_sm\_gen\_ai.sm\_mcp\_user.


## About this task

Claude Desktop supports custom MCP connectors that let Claude query external data sources on your behalf. After you add the Service Mapping MCP Server as a connector and authorize it with your ServiceNow credentials, Claude can call the Service Mapping MCP tools whenever you ask a question about application services in a chat.

For detailed information, see [Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-mcp-server.md)

## Procedure

1.  Open Claude Desktop on your computer.

2.  Open **Settings**.

3.  Select the **Connections** tab.

4.  Select **Add custom connector**.

5.  Fill in the connection details on the form.

    1.  In the **Name** field, enter a name for the connector, for example `ServiceNow Service Mapping`.

    2.  In the **Remote MCP server URL** field, enter the MCP Server URL.

    3.  Select **Advanced settings**.

    4.  In the **OAuth Client ID** field, enter the Client ID.

    5.  In the **OAuth Client Secret** field, enter the Client Secret.

6.  Select **Add**.

7.  Complete the authorization in the browser.

    1.  If prompted, enter your ServiceNow® user name and password and select **Log In**.

    2.  Review the requested permission scope and select **Allow**.

    The browser displays: Claude connected successfully. Close the browser window and return to Claude Desktop.

8.  Verify the connection.

    1.  Open a new chat in Claude Desktop.

    2.  Enter a test prompt, for example: `Use the get_all_application_service_names tool to list all application services.`

        For more information about the prompts, see [Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md).

        Claude returns a list of application service names from your ServiceNow® instance.


## Result

Claude Desktop is connected to the Service Mapping MCP Server. In any new chat, you can ask questions about your application services in natural language and Claude will query your ServiceNow® instance using the available tools.

## What to do next

For the full list of available tools, input parameters, example queries, and usage guidelines, see [Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md).

**Parent Topic:**[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/service-mapping-mcp-server.md)

