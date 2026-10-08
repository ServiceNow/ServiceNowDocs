---
title: Set up the CSM MCP Server
description: Activate the CSM MCP Server to enable AI-driven case management and GenAI skills features on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/now-assist-for-csm/activate-the-csm-mcp-server.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [CSM MCP Server, activate, GenAI, AI-driven case management, OAuth]
breadcrumb: [CSM MCP Server, ServiceNow Otto for CSM, Customer Service Management]
---

# Set up the CSM MCP Server

Activate the CSM MCP Server to enable AI-driven case management and GenAI skills features on your ServiceNow instance.

## Before you begin

The following plugins must be activated on your instance:

-   ServiceNow Otto for Customer Service Management \(CSM\) plugin \(sn\_csm\_gen\_ai\)
-   Model Context Protocol Server \(sn\_mcp\_server\)
-   CSM MCP Server \(sn\_csm\_mcp\_server\)

Role required: sn\_mcp\_server.admin or admin

## About this task

The CSM MCP Server and all associated tools are active by default.

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  From the **Configuration** tab, select **Servers**.

3.  Select the **CSM MCP Server**.

    **Note:** Change the application scope to CSM MCP Server.

    The MCP Server Console page opens with all fields populated by default.

4.  Select **Set up OAuth** to securely authenticate the CSM MCP Server with your ServiceNow instance.

    **Note:**

    -   If you use the CSM MCP Server OAuth client entry to set up your OAuth server, the fields on the Authorization code grant page are automatically populated. Use this information to connect to the CSM MCP Server.
    -   If you're setting up your own OAuth connection, the oauth\_admin or admin role is required to configure your OAuth client entry. See [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md) to set up the OAuth and connect to the CSM MCP Server.
    -   You can also create custom servers that offer different tools depending on what you need or who's using them. For step-by-step guidance on building your first custom server, check out the [Designing your first custom ServiceNow MCP server with MCP Server Console console](https://www.servicenow.com/community/servicenow-otto-articles/designing-your-first-custom-servicenow-mcp-server-with-mcp/ta-p/3566757) article in the ServiceNow Community.
5.  [Create tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/creating-tools-mcp-server.md) to connect ServiceNow with AI.

    You can build tools that let AI assistants access ServiceNow features and data through the Model Context Protocol \(MCP\). Tools control what an AI assistant can see and do in your ServiceNow instance. They define which features and information are available, and what actions the AI can take. You can create tools from different categories based on your needs.

6.  [Monitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/monitoring-dashboard.md) your MCP servers and tools.

    Use the MCP Server monitoring dashboard to track how your servers and tools are performing over any time period you choose. You can see what's working well, what failed, and any issues like throttling or access denials. This gives you a clear picture of performance, helps you spot problems, and understand what needs attention.


**Related topics**  


[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-mcp-server-console.md)

[Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md)

[Install Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-mcp-client.md)

