---
title: Azure Monitor MCP AI agent
description: This AI agent investigates Azure Monitor alerts by querying Log Analytics workspaces with KQL, retrieving platform metrics, and checking activity logs and resource health through Azure MCP tools. It returns structured findings to the parent agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-azure-monitor-mcp-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# Azure Monitor MCP AI agent

This AI agent investigates Azure Monitor alerts by querying Log Analytics workspaces with KQL, retrieving platform metrics, and checking activity logs and resource health through Azure MCP tools. It returns structured findings to the parent agent.

## Workflow

The agent investigates an Azure Monitor alert by querying Azure's monitoring data sources for supporting evidence.

1.  Identify the Azure alert and subscription to investigate from the context provided by the parent agent.
2.  Query the relevant Log Analytics workspace using KQL, applying a time window and result limit to keep queries efficient.
3.  Retrieve platform metrics, activity logs, and resource health information for the affected resource.
4.  Continue the investigation with the remaining tools if any individual call fails, noting the failure rather than stopping.
5.  Return the structured findings to the parent agent for inclusion in the overall investigation report.

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

Get Entity Health

Get Resource Health

Get VM Details

List Activity Logs

List Health Events

List Metric Definitions

List Tables

List Workspaces

Query Alert Details

Query Metrics

Query Resource Logs

Query Workspace Logs

-   **Script**

Lookup CMDB CI


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

