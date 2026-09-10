---
title: AWS CloudWatch MCP server AI agent
description: This AI agent automates AWS CloudWatch alert investigations by analyzing alarm details, querying affected resources, and retrieving CloudWatch metrics and logs across multiple strategies. It provides clear summaries with root cause analysis and actionable recommendations for resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-aws-cloudwatch-mcp-server-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# AWS CloudWatch MCP server AI agent

This AI agent automates AWS CloudWatch alert investigations by analyzing alarm details, querying affected resources, and retrieving CloudWatch metrics and logs across multiple strategies. It provides clear summaries with root cause analysis and actionable recommendations for resolution.

## Workflow

The agent investigates an AWS CloudWatch alarm, or a named entity referenced by another vendor's alert, using the CloudWatch MCP tools.

1.  Determine whether a specific CloudWatch alarm name is known, or whether the investigation must start from a named entity and work back to the relevant alarm.
2.  Retrieve the alarm's history and current state, along with its associated metric data.
3.  Analyze the relevant metrics against expected thresholds and run log insights queries against associated log groups.
4.  Review recommended metric alarms and any active alarms tied to the same resource for additional context.
5.  Summarize the findings into a clear report identifying the probable root cause and recommended remediation steps.

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

Analyze Metric

Cancel Log Insights Query

Describe Log Groups

Execute Log Insights Query

Get Active Alarms

Get Alarm History

Get Log Insights Query Results

Get Metric Metadata

Get Recommended Metric Alarms

Analyze Log Group

Get Metric Data

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

