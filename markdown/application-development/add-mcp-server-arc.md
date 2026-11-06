---
title: Add an MCP server for Arc users
description: Make a remote MCP server available to Arc users, so they can connect to it in one step without entering its details themselves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/add-mcp-server-arc.html
release: australia
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 1
keywords: [MCP server, Arc Connectors, MCP allowlist, grant type, Authorization Code \(PKCE\), Client Credentials]
breadcrumb: [Configure, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Add an MCP server for Arc users

Make a remote MCP server available to Arc users, so they can connect to it in one step without entering its details themselves.

## Before you begin

Role required: sn\_app\_arc.admin

Have the MCP server's URL and the client ID Arc uses to authenticate with it. If the server uses the Client Credentials grant type, also have its client secret and token URL.

## About this task

MCP servers you add appear first in the **Available** list in users' **MCP Servers** settings in Arc, ready to connect. Users can't edit or delete them.

## Procedure

1.  In the navigation filter, enter `sn_app_cowork_connector.list`, and press **Enter**.

    The **Arc Connectors** list opens.

2.  Select **New**.

3.  Enter a **Connector ID** and a **Display Label**, and optionally a **Description**.

4.  In the **Connector Type** field, select **MCP Server**.

5.  In the **MCP Server URL** field, enter the server's URL.

6.  In the **Grant Type** field, select how Arc authenticates with the server, and then complete the fields for that grant type.

    -   **None**: Enter the **Client ID**, and optionally the **Scopes**.
    -   **Authorization Code \(PKCE\)**: Enter the **Client ID**, and optionally the **Scopes**.
    -   **Client Credentials**: Enter the **Client ID**, **Client Secret**, and **Token URL**, and optionally the **Scopes** and **Authorization URL**.
7.  Select a **Domain**.

8.  Confirm that **Active** is selected, and then select **Submit**.


## What to do next

To stop users from using the server, open its record and clear **Active**. For more information about what users see, see [Connect ServiceNow Arc to MCP servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/connect-mcp-servers.md).

**Parent Topic:**[Configuring ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-configuring.md)

