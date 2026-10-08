---
title: Set up the Retail MCP Server
description: Install the Retail MCP Server, connect your AI client to it, and give store staff the roles they need, so they can work with Retail Service Management from their AI assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/retail-industry/rahi-retail-mcp-server-set-up.html
release: australia
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 2
keywords: [Retail MCP Server, install, OAuth, MCP client, roles]
breadcrumb: [Retail MCP Server, Configure, Retail]
---

# Set up the Retail MCP Server

Install the Retail MCP Server, connect your AI client to it, and give store staff the roles they need, so they can work with Retail Service Management from their AI assistant.

## Before you begin

These plugins must be active on the instance:

-   CSM MCP Server \(com.sn\_csm\_mcp\_server\). It also provides the platform MCP framework \(com.sn\_mcp\_server\).
-   Retail Core \(com.sn\_retail\_core\)
-   Optional: Retail Store Services \(com.sn\_rtl\_stre\_servcs\). The four case tools install only when this plugin is active.

Role required: admin

## About this task

The Retail MCP Server doesn't ship its own OAuth configuration. The platform MCP framework generates an OAuth provider and client for the server when the app is installed. Your AI client connects with that OAuth client.

## Procedure

1.  Install the Retail MCP Server application from the ServiceNow Store.

    The Retail MCP Server and its tools are registered. If Retail Store Services isn't active, only **Get my retail store** and **Get store devices** are registered.

2.  Locate the OAuth client that the platform MCP framework generated for the Retail MCP Server, in the global scope.

3.  Add callback URLs as required for MCP clients.

4.  Give the OAuth client ID and secret to the administrator of your MCP-compatible AI client, and configure the client to connect to your instance.

5.  Assign roles to the store staff who will use the tools.

    -   To find their store and devices: sn\_retail.associate\_contributor or sn\_retail.associate\_fulfiller
    -   To create, track, and update cases: sn\_rtl\_stre\_servcs.contributor
    For instructions, see [Assign roles to Retail users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-assign-roles-users.md).

6.  Make sure each user is a member of the retail store they work in.

    The tools look up a user's store from their store membership. A user who isn't a member of any store gets an empty result. For instructions, see [Add members to a retail organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-add-members-to-organization.md).


## Result

The AI client discovers the Retail MCP Server and its tools. Store staff who hold the required roles can invoke the tools from their assistant.

**Parent Topic:**[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-mcp-server-overview.md)

**Related topics**  


[Retail MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-mcp-server-overview.md)

[Retail MCP Server roles and data access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-mcp-server-access-control.md)

