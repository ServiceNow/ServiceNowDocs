---
title: CMDB MCP Server tools reference
description: The CMDB Model Context Protocol \(MCP\) Server tools let an AI agent search for and create CIs, and ask questions about the CMDB data model, with example utterances for each tool.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-ref.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [MCP Server, MCP tools, CMDB MCP]
breadcrumb: [Reference, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB MCP Server tools reference

The CMDB Model Context Protocol \(MCP\) Server tools let an AI agent search for and create CIs, and ask questions about the CMDB data model, with example utterances for each tool.

## MCP Server tools

The CMDB MCP Server exposes six tools. CMDB Search, Get Similar CI Classes, and Create CI are general availability. Get Impacted Items, Get CI Topology, and Explain CMDB Data Model are currently store-2026-09.

## CMDB Search

Searches the CMDB for CIs based on the user utterance. If the utterance resolves to a table that isn't a valid, accessible CMDB entity, the tool returns a validation error.

|Parameter|Required|Description|
|---------|--------|-----------|
|**utterance**|Conditional|Natural language search query, for example "find all linux servers". Required unless **cisysid** is provided.|
|**cisysid**|Conditional|Limits the search to the Configuration Item \[cmdb\_ci\] record with this sys\_id. Required unless **utterance** is provided.|
|**groupby**|Optional|Field name used to group search results.|

|Match count|Response|
|-----------|--------|
|No matches|A message stating that no records matched the search.|
|Single match|The matching CI's sys\_id, table, name, class, and a summary, plus links to the CI's form and map views.|
|2 to 10 matches|A list of the matching CIs, each with sys\_id, name, class, table, and last updated date, plus a link to the full list.|
|More than 10 matches|Results grouped by CI class or by the **groupby** field, up to 20 groups, with a count for each group. If the specified **groupby** field isn't valid for the table, the response falls back to grouping by CI class and includes a warning.|

Example utterances:

-   "Find all Linux servers in the CMDB."
-   "Search for CIs with a non-operational status, grouped by CI class."

## Get Similar CI Classes

Finds CI classes that match a specified name or keyword. Use this tool before creating a CI to identify the correct technical class name and its required attributes.

|Parameter|Required|Description|
|---------|--------|-----------|
|**class\_name**|Required|CI class name or keyword to search for, for example "linux server" or "cmdb\_ci\_win\_server".|

On a match, the tool returns up to five candidate CI classes, each with its display label and technical class name. If no class matches the provided name, the tool returns an error. The error message notes that creation can still be attempted directly with a technical class name, though it's unlikely to succeed.

Example utterances:

-   "What CI class should I use for a Linux server?"
-   "Find CI classes similar to cmdb\_ci\_win\_server."

## Create CI

Creates a new CI for a specified CI class with the provided attributes. Before using this tool, use Get Similar CI Classes to confirm the correct class name and required fields.

|Parameter|Required|Description|
|---------|--------|-----------|
|**ci\_class\_name**|Required|Technical name of the CI class, for example "cmdb\_ci\_linux\_server".|
|**attributes\_map**|Required|Key-value pairs of CI attribute names and values.|

On success, the tool returns a confirmation message with a link to the new CI in CMDB Workspace. If required attributes are missing, if a matching CI already exists, or if the CI can't be created, the tool returns an error describing the problem.

Example utterances:

-   "Create a CI for a Linux server named app-db-03 with IP address 10.10.5.42."
-   "Create a new CMDB CI for an app server called payment-gateway-02."

## Get Impacted Items

Returns the CIs, services, and teams impacted by a given change request, using the Impact Analysis Skill capability.

|Parameter|Required|Description|
|---------|--------|-----------|
|**change\_request\_number**|Required|The change request number to analyze for impact, for example **CHG0001234**.|

On success, the tool returns the impacted-items list produced by the Impact Analysis Skill capability. See [Assess CMDB impact agentic workflow reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-ref.md) for the full output schema, including impact level, impact type, and confidence for each impacted CI. If **change\_request\_number** is missing, or the Impact Analysis Skill capability doesn't complete successfully, the tool returns an error describing the problem.

Example utterances:

-   "What CIs are impacted by change CHG0001234?"
-   "Use the CMDB MCP Server tool, Get Impacted Items, to check the blast radius of change CHG0005678."

## Get CI Topology

Returns the CI topology as nodes and edges, including upstream and downstream relationships. If the topology exceeds the node limit, the response is truncated and includes a warning.

|Parameter|Required|Description|
|---------|--------|-----------|
|**ci\_sys\_id**|Required|The sys\_id of a record in the Configuration Item \[cmdb\_ci\] table. The tool verifies the CI exists before building its topology.|

On success, the tool returns the topology's nodes, edges, and root CI. If the traversal reaches the node limit, the response also includes a truncation flag and a warning message. If **ci\_sys\_id** is missing, or doesn't match an existing CI, the tool returns an error.

Example utterances:

-   "Show me the topology for this CI, including everything upstream and downstream."
-   "Use the CMDB MCP Server tool, Get CI Topology, to map dependencies for the server I just found."

## Explain CMDB Data Model

Answers natural language questions about the CMDB data model, including classes, tables, fields, and relationships, using the Data Model Navigator \(DMN\) agent. See [Data Model Navigator app features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-data-model-nav-ref.md) for the agent's own reference documentation.

|Parameter|Required|Description|
|---------|--------|-----------|
|**user\_query**|Required|Natural language question about the CMDB data model, for example "What fields does the cmdb\_ci\_server table have?"|

|Match type|Fields returned|
|----------|---------------|
|Field|Field name and description, sample data, the owning table and its description, and a relevance score.|
|Table|Table name, table description, and a relevance score.|
|Business context|Context name, context description, and a relevance score.|
|Relationship|Source table, target table, and a description of the relationship. Results are limited to 5 relationships per table and 15 relationships total.|

If **user\_query** is missing, or the requester doesn't have the required roles, the tool returns an error.

Example utterances:

-   "What fields does the cmdb\_ci\_server table have?"
-   "How is the cmdb\_ci table related to cmdb\_rel\_ci?"

## Role access

Access to each tool is controlled by the role specified in the prerequisites of [Activate the CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server.md).

**Parent Topic:**[ServiceNow Otto for CMDB reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-reference.md)

**Related topics**  


[CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server-c.md)

[Activate the CMDB MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-mcp-server.md)

[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.md)

[Assess CMDB impact agentic workflow reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-ref.md)

