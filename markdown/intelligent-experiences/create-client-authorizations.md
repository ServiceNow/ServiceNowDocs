---
title: Create client authorizations
description: Establish connections between your MCP clients and servers with client authorizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-client-authorizations.html
release: zurich
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
keywords: [client authorization]
breadcrumb: [Create an OAuth inbound integration for an MCP client, Connect, MCP Server Console, Enable AI experiences]
---

# Create client authorizations

Establish connections between your MCP clients and servers with client authorizations.

## Before you begin

Role required: sn\_mcp\_server.admin \(create\); sn\_mcp\_server.viewer \(to view\)

## About this task

Explore an alternate way of OAth creation with Client Authorization option within the left navigation of MCP Server Console. The process of creating an MCP Server by integrating OAuth Client registration directly within the MCP Server Console is streamlined. This feature eliminates the need to switch between different consoles. You don’t have to leave the Machine Identity Console to register an OAuth Client, manually copy secrets and return to complete the MCP Client setup.

The the OAuth fields are auto-populated, generating the Client ID and Secret without the need for navigation, and providing a one-time Connection Summary that displays the necessary credentials.

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console** &gt; **Servers**.

2.  You can also navigate to **Admin** &gt; **MCP Server Console** &gt; **Servers**.

3.  Select **Client authorization** on the left navigation.

4.  Review all the authorization details that you will need, to integrate the MCP client.

    See [Configure an MCP client to connect to an MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-client-connect-server.md) to details on these URLs.

    -   Authorization URL
    -   Token URL
    -   Refresh URL
    -   Host URL
5.  Select **Create integration**.

6.  Enter a name for the OAuth integration you create.

7.  Enter the redirect URL associated with your MCP client.

    \[Omitted image "mcp-create-oath-int.png"\] Alt text: Create an OAth integration

8.  Select **Create**.

9.  Select the authorization client you created.

    The client summary with details like Client ID and Client secret is displayed.

    \[Omitted image "mcp-create-oath-client-summ.png"\] Alt text: Client summary for OAuth creation

10. Copy the Client ID, Client Secret, Redirect URL, and connection URLs using the copy options.

11. Enter these details on the MCP client's OAuth configuration.

    MCP Server and Client connection is established with client authorization.


## What to do next

Configure the MCP Client to connect to MCP Server. See [Configure an MCP client to connect to an MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-client-connect-server.md).

**Parent Topic:**[Create an OAuth inbound integration for an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-oauth-inbound-integration-mcp-client.md)

