---
title: Access Enterprise Architecture data using MCP tools
description: Use MCP tools to query live Enterprise Architecture data—including business application insights, capability mappings, architectural relationships, and rationalization data—from any MCP-compatible AI assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-portfolio-management/access-ea-data-using-mcp-tools.html
release: australia
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [MCP tools, Enterprise Architecture, business application insights, capability mapping, EA MCP server]
breadcrumb: [Use, MCP for Enterprise Architecture, Enterprise Architecture]
---

# Access Enterprise Architecture data using MCP tools

Use MCP tools to query live Enterprise Architecture data—including business application insights, capability mappings, architectural relationships, and rationalization data—from any MCP-compatible AI assistant.

## Before you begin

Role required: sn\_mcp\_server.viewer and sn\_apm.apm\_read or sn\_apm.apm\_user

## About this task

When you send a message, the AI assistant selects the relevant MCP tool from the available tools and retrieves the requested EA data. For a list of available tools, see [Explore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/exploring-ea-mcp-server.md).

**Note:** This procedure uses Claude as an example AI assistant. Steps may vary depending on the AI client you use.

## Procedure

1.  Open the Claude application on your computer.

2.  Start a chat by sending a message such as `Show me the business applications that support the Finance capability`.

    The Capability Hierarchy App Resolver tool retrieves applications mapped to the specified capability and its child capabilities.

3.  Continue the conversation to retrieve additional data — for example, send `Show me insights for the first application`.

    The Get EA Business App Insights tool generates Now Assist AI-powered insights for the specified business application.

4.  Continue the conversation with additional prompts to retrieve the data you need.

    Example prompts you can use:

    -   `Which applications are at risk based on rationalization scores?`—uses the App Rationalization Query tool.
    -   `What entities are related to Workday?`—uses the Related Entities Resolver tool.
    -   `What changed in this diagram compared to last month?`—uses the Diagram change analysis tool.
    -   `Which entities does the Procure to Pay architecture diagram document?`—uses the Artifact Resolver tool.
    -   `Which business capabilities are impacted if the PS ORA01 database fails?`—uses the Related Entities Resolver tool to trace dependencies across multiple levels.

**Parent Topic:**[Using MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/using-ea-mcp-server.md)

**Related topics**  


[Working with Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/ea-qna-use.md)

[Generate insights into business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/generate-insights-into-ba.md)

[Compare Enterprise Modeling and Visualization diagrams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/compare-modeling-diagrams.md)

[Working with application rationalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-work-with-app-rat.md)

[Working with the business portfolio module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-work-with-business-portfolio-mod.md)

[Enterprise Architecture Workspace access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-access-roles.md)

