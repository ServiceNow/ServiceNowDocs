---
title: Explore
description: MCP for Enterprise Architecture provides enterprise architects and application portfolio managers direct access to business application insights, capability mappings, architectural relationships, and rationalization data in their AI client. Opening the ServiceNow instance is not required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-portfolio-management/exploring-ea-mcp-server.html
release: australia
topic_type: concept
last_updated: "2026-10-03"
reading_time_minutes: 3
keywords: [EA MCP server]
breadcrumb: [MCP for Enterprise Architecture, Enterprise Architecture]
---

# Explore

MCP for Enterprise Architecture provides enterprise architects and application portfolio managers direct access to business application insights, capability mappings, architectural relationships, and rationalization data in their AI client. Opening the ServiceNow instance is not required.

## MCP for Enterprise Architecture overview

The Enterprise Architecture \(EA\) Model Context Protocol \(MCP\) server connects an AI assistant such as Claude to your ServiceNow instance. Ask natural language questions to retrieve business application data, capability mappings, architectural relationships, and rationalization insights — without navigating through tabs and reports.

## MCP for Enterprise Architecture personas

|Persona|Description|
|-------|-----------|
|Enterprise architect|Queries architectural relationships, reviews diagram comparisons, and retrieves business application insights to support roadmap and rationalization decisions.|
|Application portfolio manager|Accesses business application data, capability mappings, and rationalization scores to prioritize investment and plan modernization initiatives.|

## Available tools

Access Enterprise Architecture data and Now Assist AI skills as MCP tools, enabling LLM \(large language model\) agents to query and process business applications, capabilities, architectural relationships, and diagrams.

The tools installed with the application are annotated as read-only. They retrieve or analyze EA data but don't create, update, or delete records in your instance. For details about tool annotations, see [Components installed with MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/installed-with-mcp-for-ea.md). For the parameters that each tool accepts, see [MCP for Enterprise Architecture tool parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/ea-mcp-server-tool-parameters.md).

The following tools are available:

|Tool name \[ID\]|Description|
|----------------|-----------|
|App Rationalization Query \(sn\_ea\_mcp\_server.ea.app\_rationalization\_query\)|Retrieves and scores business applications based on rationalization criteria, supporting portfolio investment and modernization decisions.|
|Capability Hierarchy App Resolver \(sn\_ea\_mcp\_server.ea.capability\_hierarchy\_resolver\)|Resolves business capability-to-application mappings by traversing the capability hierarchy, identifying which applications support each capability at every level.|
|Related Entities Resolver \(sn\_ea\_mcp\_server.ea.related\_entities\_resolver\)|Retrieves entities related to a specified business application or architectural element, identifying dependencies and relationships across the EA data model. Also traces multi-level impact and dependency chains from a single configuration item, for example, the business capabilities affected if a database fails.|
|Get EA Business App Insights \(sn\_ea\_mcp\_server.ea.get\_ea\_business\_app\_insights\)|Generates Now Assist AI-powered insights for a business application, including health scores, rationalization signals, and strategic recommendations.|
|Enterprise Graph \(sn\_mcp\_server.enterprise\_graph\)|Queries the EA knowledge graph to answer natural language questions about architectural relationships, business capabilities, and technology product connections across the enterprise. Enterprise Graph is a platform tool that's associated with the EA MCP server, rather than installed with the application.|
|Diagram change analysis \(sn\_ea\_mcp\_server.diagram\_change\_analysis\)|Compares two versions of an EA diagram and summarizes the architectural changes between them. Can also summarize a single diagram version. Available only when the Enterprise Modeling and Visualization plugin is installed.|
|Artifact Resolver \(sn\_ea\_mcp\_server.ea.artifact\_resolver\)|Identifies the architectural artifacts, such as documents and diagrams, that are linked to an EA entity, and the entities that a given artifact documents.|

## Related topics

To learn more about configuring and using MCP for Enterprise Architecture, see the following topics.

-   [Configuring MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/configuring-ea-mcp-server.md)
-   [Using MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/using-ea-mcp-server.md)
-   [MCP for Enterprise Architecture reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/reference-ea-mcp-server.md)

**Parent Topic:**[MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/ea-mcp-server-landing-page.md)

**Related topics**  


[Exploring ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/exploring-now-assist-for-ea.md)

[Exploring Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/ea-qna-overview.md)

[Enterprise Architecture Workspace access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-access-roles.md)

