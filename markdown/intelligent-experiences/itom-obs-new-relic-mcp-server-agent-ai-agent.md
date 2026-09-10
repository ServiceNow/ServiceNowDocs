---
title: New Relic MCP server AI agent
description: This AI agent queries and interprets observability data from New Relic using the full suite of New Relic MCP server tools. It answers questions about entity health, service dependencies, log analysis, alert details and history, performance metrics, and change events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-new-relic-mcp-server-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# New Relic MCP server AI agent

This AI agent queries and interprets observability data from New Relic using the full suite of New Relic MCP server tools. It answers questions about entity health, service dependencies, log analysis, alert details and history, performance metrics, and change events.

## Workflow

The agent investigates a New Relic alert or answers a direct question using New Relic observability data.

1.  Determine whether the request is driven by a New Relic alert issue or by a direct conversational question.
2.  Identify the relevant entity, service, or issue to investigate based on that context.
3.  Query New Relic for entity health, performance metrics, logs, and related change events using the appropriate MCP tools.
4.  Review alert conditions, policies, and recent issues associated with the entity for additional context.
5.  Translate the findings into clear, structured answers for the calling agent or user, without exposing internal system details.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Model Context Protocol tools**

Analyze Deployment Impact

Analyze Entity Logs

Analyze Golden Metrics

Analyze Kafka Metrics

Analyze Threads

Analyze Transactions

Convert Time Period to Epoch

Execute NRQL Query

Generate Alert Insights Report

Generate User Impact Report

Get Dashboard

Get Entity

List Alert Conditions

List Alert Policies

List Available Accounts

List Change Events

List Dashboards

List Entity Error Groups

List Entity Types

List Garbage Collection Metrics

List Recent Issues

List Recent Logs

List Related Entities

List Synthetic Monitors

Natural Language to NRQL

Search Entity by Tag

Search Incidents


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

evt\_mgmt\_operator

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

evt\_mgmt\_operator

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>For more information, see [ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-health-landing-page.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-ai-agents-overview.md)

