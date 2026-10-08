---
title: Components installed with MCP for Enterprise Architecture
description: The MCP for Enterprise Architecture plugin installs tools, scripted REST APIs, and access controls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-portfolio-management/installed-with-mcp-for-ea.html
release: australia
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [EA MCP server]
breadcrumb: [Reference, MCP for Enterprise Architecture, Enterprise Architecture]
---

# Components installed with MCP for Enterprise Architecture

The MCP for Enterprise Architecture plugin installs tools, scripted REST APIs, and access controls.

## Tools installed

|Tool name \[ID\]|Description|
|----------------|-----------|
|App Rationalization Query \(sn\_ea\_mcp\_server.ea.app\_rationalization\_query\)|Retrieves and scores business applications based on rationalization criteria, supporting portfolio investment and modernization decisions.|
|Capability Hierarchy App Resolver \(sn\_ea\_mcp\_server.ea.capability\_hierarchy\_resolver\)|Resolves business capability-to-application mappings by traversing the capability hierarchy, identifying which applications support each capability at every level.|
|Related Entities Resolver \(sn\_ea\_mcp\_server.ea.related\_entities\_resolver\)|Retrieves entities related to a specified business application or architectural element, and returns dependencies and relationships across the EA data model. It also traces multi-level impact and dependency chains from a single configuration item.|
|Get EA Business App Insights \(sn\_ea\_mcp\_server.ea.get\_ea\_business\_app\_insights\)|Generates Now Assist AI-generated insights for a business application, including health scores, rationalization signals, and strategic recommendations.|
|Diagram change analysis \(sn\_ea\_mcp\_server.diagram\_change\_analysis\)|Compares two versions of an EA diagram and summarizes the architectural changes between them. Can also summarize a single diagram version. Available only when the Enterprise Modeling and Visualization plugin is installed.|
|Artifact Resolver \(sn\_ea\_mcp\_server.ea.artifact\_resolver\)|Identifies the architectural artifacts, such as documents and diagrams, that are linked to an EA entity, and the entities that a given artifact documents.|

**Note:**

-   A tool's annotation defines the operations that the tool can perform on your instance data. All tools installed with the application have the readOnlyHint annotation, which means they retrieve data but don't create, update, or delete records. To view a tool's annotation, open the tool record in the MCP Server Console Console and see the **Annotations** field.
-   The EA MCP server is also associated with the Enterprise Graph tool \(sn\_mcp\_server.enterprise\_graph\). This tool is provided by the platform and isn't installed with the application.

## Scripted REST APIs installed

|Scripted REST API \[API ID\]|Description|
|----------------------------|-----------|
|EA MCP Tool API \(ea\_mcp\_tools\)|Provides the endpoints for retrieving EA data. The Get EA Business App Insights, Capability Hierarchy App Resolver, App Rationalization Query, Related Entities Resolver, and Artifact Resolver tools call these endpoints.|

## Access controls installed

|Access control|Description|
|--------------|-----------|
|EA MCP Tool API|Restricts access to the EA MCP Tool API endpoints to users with the sn\_apm.apm\_read or sn\_apm.apm\_user role.|

**Parent Topic:**[MCP for Enterprise Architecture reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/reference-ea-mcp-server.md)

**Related topics**  


[eaw-installed-with-eaw]

[Enterprise Architecture Workspace access roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-portfolio-management/eaw-access-roles.md)

