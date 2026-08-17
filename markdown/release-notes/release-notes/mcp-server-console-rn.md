---
title: MCP Server Console release notes
description: The ServiceNow MCP Server Console application enables secure and governed access to functionality on a ServiceNow instance for AI applications with Model Context Protocol \(MCP\) servers. MCP servers extend ServiceNow AI Platform functionality into any external MCP client and employee experience over the Model Context Protocol. MCP Server Console is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-04"
reading_time_minutes: 3
---

# MCP Server Console release notes

The ServiceNow® MCP Server Console application enables secure and governed access to functionality on a ServiceNow instance for AI applications with Model Context Protocol \(MCP\) servers. MCP servers extend ServiceNow AI Platform® functionality into any external MCP client and employee experience over the Model Context Protocol. MCP Server Console is a new application in the Zurich release.

## MCP Server Console highlights for the Zurich release

-   Unify the MCP Server creation process by embedding OAuth Client registration directly within the MCP Server Console wizard. This eliminates the need for users to switch contexts between multiple consoles.
-   Enable administrators to configure annotations across all supported tool types. Annotations will be included in the tools/list response per MCP specification, allowing MCP clients like Claude to apply correct permission policies.
-   Get started with the preconfigured Quickstart Server for looking up and summarizing incident and case records.
-   Create MCP apps to implement and manage interactive interfaces for your tools that can be displayed by MCP clients.
-   Integrate third-party identity provider \(IDP\) with MCP server to support users authentication through a third-party \(IDP\).
-   Create MCP Server Console servers and tools based on various categories including Now Assist skills for different use cases.
-   Connect to any MCP Server Console client using OAuth 2.0 authentication.

See [MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/mcp-platform-manager-landing.md) for more information.

**Important:** MCP Server Console is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## MCP Server Console features

-   ****

    The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own

-   **[Create tools from additional capabilities for use with ServiceNow MCP clients](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-tool-mcp-server.md)**

    With this release, you can now create tools from additional categories like, Knowledge graphs, Subflow, Action, and REST APIs and Now Assist skills.


-   **[Create tools from additional capabilities for use with ServiceNow MCP clients](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-tool-mcp-server.md)**

    With this release, Moveworks is shipping a Moveworks Quickstart Server. This server allows users to pilot access to upcoming capabilities like Knowledge graph, Subflow, Action, and scripted REST APIs for use with Moveworks MCP client, and ServiceNow Model Context Protocol Client application. These tools can only be added to Moveworks Quickstart Server.


-   **[Get started with the preconfigured Quickstart Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-mcp-server-console.md)**

    Learn about MCP Server Console and connecting MCP Server Console clients to a ServiceNow instance with the preconfigured Quickstart Server. The Quickstart Server includes tools for looking up and summarizing incident and case records.

-   **[Create MCP servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-mcp-server.md)**

    Create MCP Server Console servers that expose different tools for different use cases, such as for HR or IT workflows, or for different MCP Server Console clients.

-   **[Create tools from Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-tool-mcp-server.md)**

    Create tools for MCP Server Console servers from Now Assist skills and configure which fields are exposed as tool inputs.

-   **[Connect to MCP clients using an OAuth inbound integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/connect-mcp-server-client.md)**

    Create an OAuth inbound integration to use when configuring MCP Server Console clients to connect to an MCP Server Console server.


## Activation information

MCP Server Console is available with activation of a Now Assist application. For more information, see [Installing Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/installing-generative-ai-controller.md) and [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Plugin information

-   **New plugins**

    The following plugins are new in Zurich:

    Model Context Protocol Server \(sn\_mcp\_server\): MCP Server Console enables secure and governed access to functionality on a ServiceNow instance for AI applications with Model Context Protocol \(MCP\) servers.


## Related ServiceNow applications and features

-   **[AI Control Tower \(legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-control-tower-landing.md)**

    AI Control Tower enables enterprises to manage, optimize, govern, secure, and measure the value of their AI investments. AI Gateway in AI Control Tower is a registry for MCP Server Console servers and provides observability and metrics for servers and their tools.

-   **[Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/mcp-client.md)**

    The ServiceNow® Model Context Protocol Client enables you to access the Model Context Protocol tools that are hosted externally and published using an MCP server in AI Agent Studio.

-   **[Machine Identity Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/machine-identity-console.md)**

    Create and manage OAuth inbound integrations to connect MCP Server Console clients to servers in Machine Identity Console.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

