---
title: Dynatrace MCP server AI agent
description: This agent investigates Dynatrace alerts by retrieving alert impact summaries and querying the Dynatrace API for problem details, entity enrichment, log analysis, and root cause theories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-dynatrace-mcp-server-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Dynatrace MCP server AI agent

This agent investigates Dynatrace alerts by retrieving alert impact summaries and querying the Dynatrace API for problem details, entity enrichment, log analysis, and root cause theories.

## Workflow

1.  Identify what to investigate.

    The agent uses a Dynatrace problem ID or a provided entity name to determine what to investigate.

2.  Gather relevant problem details, entity information, spans, and logs from Dynatrace.
3.  Return the findings, including a problem overview, key findings, and actionable next steps.

For more information about configuring this AI agent, see [Configure observability agents for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/configure-integration-agents-for-now-assist.md).

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Model Context Protocols**

Data Analysis Agent

DQL Explanation Agent

Forecasting Agent

Grail Query Agent

Help Agent

Kubernetes Agent

Root Cause Agent

Root Cause Details Agent

Vulnerability Agent


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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

[Analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/now-assist-itom-agentic-aia.md)

</td></tr></tbody>
</table>For more information, see [ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-health-landing-page.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itom-ai-agents-overview.md)

