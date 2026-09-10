---
title: Knowledge Graph schema support in MCP Server Console
description: MCP Server Console supports creating tools from several preconfigured Knowledge Graph schemas, each suited to different types of queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/knowledge-graph-support-mcp.html
release: australia
topic_type: reference
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [Knowledge Graph schemas for MCP]
breadcrumb: [Reference, MCP Server Console, Enable AI experiences]
---

# Knowledge Graph schema support in MCP Server Console

MCP Server Console supports creating tools from several preconfigured Knowledge Graph schemas, each suited to different types of queries.

The following Knowledge Graph schemas are available by default when creating a tool from a Knowledge Graph. Select a schema based on the type of query your tool needs to run and how the underlying tables are used across your instance.

**Tip:** Start with Enterprise Graph \(Small\). Move to the full Enterprise Graph only if your workflows require cross-domain traversal that the smaller schema doesn't cover. For people and organizational structure queries, User Graph or NLQ User Graph is the more targeted choice.

|Schema|Description|
|------|-----------|
|Enterprise Graph|Covers all tables on your instance. Best for complex queries that span multiple domains.|
|Enterprise Graph \(Small\)|A curated subset of the most commonly queried tables. Faster and more token-efficient than the full Enterprise Graph. Best starting point for most IT and HR workflows.|
|User Graph|Focused on people, organizational structure, roles, and relationships. Best for organization hierarchy look ups or manager relationships.|
|NLQ User Graph|A variant of the User Graph schema optimized for natural language queries. Consult your implementation guide for specific use cases.|
|Table Look up Graph|Designed for structured table and record look ups. Consult your implementation guide for specific use cases.|
|Identify Survey Instance|A specialized schema for survey-related workflows. Consult your implementation guide for specific use cases.|

**Parent Topic:**[MCP Server Console reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mcp-server-console-reference.md)

**Related topics**  


[Create a tool from a Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a-tool-from-knowledge-graphs.md)

[Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md)

