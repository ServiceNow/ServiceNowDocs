---
title: AWS CloudWatch API AI agent
description: This AI agent investigates AWS CloudWatch alarm firings end to end by querying alarm configuration, metric time series, log groups, ML anomaly detectors, and Logs Insights. It then synthesizes findings into a structured root cause analysis report with metric analysis, log evidence, and correlated service impact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/itom-obs-aws-cloudwatch-api-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# AWS CloudWatch API AI agent

This AI agent investigates AWS CloudWatch alarm firings end to end by querying alarm configuration, metric time series, log groups, ML anomaly detectors, and Logs Insights. It then synthesizes findings into a structured root cause analysis report with metric analysis, log evidence, and correlated service impact.

## Workflow

1.  Identify what to investigate.

    The agent uses either the provided CloudWatch alarm name and region or entity name and region.

2.  Gather context about the resource and investigate metrics and logs.
3.  Return findings, including a summary of probable causes, recommended next steps, and investigation notes.

For more information about configuring this AI agent, see [Configure observability agents for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configure-integration-agents-for-now-assist.md).

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Flow Actions**

Analyze Log Group

Get Alarm Details

Get Log Groups

Get Metric Data

Get Resource Tags

-   **Script**

Lookup CMDB CI

-   **Subflow**

Query Logs


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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

[Analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/now-assist-itom-agentic-aia.md)

</td></tr></tbody>
</table>For more information, see [ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-health-landing-page.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-ai-agents-overview.md)

