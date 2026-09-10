---
title: CMDB MCP Server
description: The CMDB MCP Server exposes CMDB capabilities to external AI clients using the Model Context Protocol \(MCP\), so those clients can work with your configuration data without direct database access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-c.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 2
keywords: [MCP Server, Model Context Protocol, CMDB MCP]
breadcrumb: [Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB MCP Server

The CMDB MCP Server exposes CMDB capabilities to external AI clients using the Model Context Protocol \(MCP\), so those clients can work with your configuration data without direct database access.

MCP gives AI clients structured, secured, tool-based access to your data in the ServiceNow® instance. The CMDB MCP Server exposes CMDB capabilities as MCP tools that AI clients can call directly.

## Supported clients

The MCP Server supports the Claude Desktop and Moveworks MCP clients.

## Available tools

The MCP Server provides the following tools:

|Tool|Description|
|----|-----------|
|CMDB Search|Searches the CMDB for CIs based on the user utterance.|
|Get Similar CI Classes|Finds CI classes that match a specified name or keyword. Use this tool before creating a CI to identify the correct technical class name and its required attributes.|
|Create CI|Creates a new CI for a specified CI class with the provided attributes. Before using this tool, use Get Similar CI Classes to confirm the correct class name and required fields.|
|Get Impacted Items|Returns the CIs, services, and teams impacted by a given change request, using the Impact Analysis Skill capability.|
|Get CI Topology|Returns the CI topology as nodes and edges, including upstream and downstream relationships.|
|Explain CMDB Data Model|Answers natural language questions about the CMDB data model, including classes, tables, fields, and relationships, using the Data Model Navigator \(DMN\) agent.|

For detailed input and output specifications for each tool, including example utterances, see [CMDB MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-ref.md).

## Setting up the MCP Server

To activate the MCP Server and control access to it, see [Activate the CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server.md).

**Parent Topic:**[Using agentic workflows in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

**Related topics**  


[Activate the CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server.md)

[CMDB MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-ref.md)

[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.md)

