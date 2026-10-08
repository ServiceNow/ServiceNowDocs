---
title: CSM MCP Server tools reference
description: Reference for all tools available in the CSM MCP Server, organized by functional area: case management and GenAI skill tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/csm-mcp-server-tools-reference.html
release: brazil
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [CSM MCP Server, ServiceNow Otto for CSM, Customer Service Management]
---

# CSM MCP Server tools reference

Reference for all tools available in the CSM MCP Server, organized by functional area: case management and GenAI skill tools.

**Important:**

-   Only the tools listed here are available. If any other tools are displayed in the Tools definition, you must review and resolve the skipped records for those tools. For information on reviewing and resolving skipped records, see [Review skipped records using related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/uc-access-rl.md).
-   You need the sn\_mcp\_server.viewer role as the base role to access CSM MCP server tools. For more information, see [Configure an MCP client to connect to an MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-client-connect-server.md).

## Case management tools

The following tools are available for case management in the CSM MCP Server.

|Tool name|Description|
|---------|-----------|
|get\_case\_tasks|Get list of case tasks for given criteria or details of specific case tasks|
|get\_customer\_service\_cases|Get list of cases for given criteria or get details of specific case|

## GenAI skill tools

The following tools are available for GenAI skills in the CSM MCP Server.

|Tool name|Description|
|---------|-----------|
|case\_summarization|Summarizes case activity, key actions, and current status|
|resolution\_notes\_generation|Generates a draft resolution notes entry for the case|
|sentiment\_analysis|Evaluates the sentiment of a CSM case using the Sentiment Analysis GenAI skill. Returns sentiment score, trend, and reasoning. Enforces record-level read access before invoking the skill.|
|activity\_response|Generates an AI-drafted activity response for a CSM case using the Activity Response Generation skill. Supports three response modes: Respond, Follow-Up, Summarize.|

The GenAI skill tools use the MCP Skill API, which allows only the `sn_customerservice_agent` and `sn_customerservice.consumer_agent` roles.

