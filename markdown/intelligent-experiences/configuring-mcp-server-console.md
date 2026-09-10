---
title: Configuring MCP Server Console
description: Create a Model Context Protocol \(MCP\) server and configure the tools and inputs it exposes to MCP clients.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/configuring-mcp-server-console.html
release: zurich
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [configure]
breadcrumb: [MCP Server Console, Enable AI experiences]
---

# Configuring MCP Server Console

Create a Model Context Protocol \(MCP\) server and configure the tools and inputs it exposes to MCP clients.

## Configuration overview

1.  [Create a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-mcp-server.md)

    An AI administrator creates a server and adds tools to the server.

2.  [Creating tools for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/creating-tools-mcp-server.md)

    If additional tools are needed, the AI administrator identifies which functionality to expose and creates tools based on AI skills. From the tools, they configure which fields are exposed to clients as tool inputs.

3.  [Create an MCP app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-an-mcp-app.md)

    Optionally, the AI administrator can also create an MCP app to deliver an interactive interface for tools that can be displayed by clients.


After configuring a server, the AI administrator configures OAuth inbound integrations for each client or configures an integration with a third-party identity provider \(IDP\) for authentication. Then they can configure clients to connect to the server using the server and authentication details. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/connect-mcp-server-client.md).

-   **[Create a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-mcp-server.md)**  
Create a Model Context Protocol \(MCP\) server and configure which tools it exposes to MCP clients.
-   **[Creating tools for a Model Context Protocol server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/creating-tools-mcp-server.md)**  
You can create tools from various tool categories to expose ServiceNow capabilities to Model Context Protocol \(MCP\) clients from MCP servers.
-   **[Create an MCP app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-an-mcp-app.md)**  
Build, register, and display user interfaces along with your tool's logic with MCP apps. This allows you to implement and manage interactive interfaces for your tools that can be displayed by MCP clients.
-   **[Create an AI ACL for a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-acl.md)**  
Create the necessary AI Access Control List \(ACL\) for the component to be called externally.
-   **[Check the compatibility of a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/check-compatibility-of-subflow.md)**  
After establishing the ACL, publish the component and check the compatibility staging table.

**Parent Topic:**[MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)

