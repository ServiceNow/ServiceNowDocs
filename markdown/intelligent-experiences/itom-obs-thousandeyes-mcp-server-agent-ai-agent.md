---
title: ThousandEyes MCP server AI agent
description: This AI agent investigates ThousandEyes tests. It retrieves test configuration, analyzes metrics and anomalies, correlates network events and outages, and performs path visualization to provide actionable root cause analysis. It receives a test ID and optional alert context from the orchestrator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-thousandeyes-mcp-server-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# ThousandEyes MCP server AI agent

This AI agent investigates ThousandEyes tests. It retrieves test configuration, analyzes metrics and anomalies, correlates network events and outages, and performs path visualization to provide actionable root cause analysis. It receives a test ID and optional alert context from the orchestrator.

## Workflow

The agent investigates a ThousandEyes test to determine the root cause of a triggered alert or a cross-referenced network issue.

1.  Identify the ThousandEyes test associated with the alert, either from a provided test ID or test name, or by matching a named host or service to its monitoring test.
2.  Retrieve the test's configuration details, including its type, interval, and monitoring agent locations.
3.  Collect the relevant performance metrics and detect anomalies for the test over an appropriate time window around the alert.
4.  Check for related network events and internet service provider outages that could explain the issue.
5.  Run network path visualization for test types where a network path is relevant, analyzing hop-by-hop packet loss and latency.
6.  Review ownership tags and labels associated with the test to identify the responsible team or business unit.
7.  Summarize the findings into a structured report, including probable root cause and recommended next steps.

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

Get Anomalies

Get Event Details

Get Metrics

Get Path Visualization

Get Test Details

List Events

List Tags

List Tests

Search Outages


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

