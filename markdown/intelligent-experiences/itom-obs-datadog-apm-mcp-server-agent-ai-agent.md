---
title: Datadog APM MCP server AI agent
description: This AI agent queries Datadog APM observability data using the full suite of Datadog MCP server tools. It can answer questions about service health, distributed traces, triggered monitors, log analysis, incidents, SLO compliance, deployment events, and service dependencies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-datadog-apm-mcp-server-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# Datadog APM MCP server AI agent

This AI agent queries Datadog APM observability data using the full suite of Datadog MCP server tools. It can answer questions about service health, distributed traces, triggered monitors, log analysis, incidents, SLO compliance, deployment events, and service dependencies.

## Workflow

The agent investigates a Datadog alert, a cross-referenced entity, or a direct user question about Datadog observability data.

1.  Determine whether the request is driven by a Datadog alert, a cross-referenced entity from another vendor's alert, or a direct conversational question.
2.  Identify the relevant monitor, service, or entity to investigate based on that context.
3.  Query Datadog for service health, distributed traces, logs, incidents, and deployment events relevant to the issue.
4.  Check service level objective compliance and service dependency data where relevant to the investigation.
5.  Translate the findings into clear, structured answers for the calling agent or user, avoiding any exposure of internal system details.

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

Get Datadog Dashboard

Get Datadog Incident

Get Datadog Metric

Get Datadog Trace

Search Datadog Dashboards

Search Datadog Events

Search Datadog Incidents

Search Datadog Logs

Search Datadog Monitors

Search Datadog Service Dependencies

Search Datadog Services

Search Datadog SLOs

Search Datadog Spans


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

