---
title: Issue trend analysis AI agent
description: This AI agent analyzes grouped task data from cases, incidents, problems, or other tables to identify recurring issues and root causes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-issue-trend-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Issue trend analysis AI agent

This AI agent analyzes grouped task data from cases, incidents, problems, or other tables to identify recurring issues and root causes.

## Workflow

The agent provides detailed, actionable recommendations through structured analysis.

1.  Extract the record type from the user's input.
2.  Pass the extracted record types to the Get Task Analysis Config tool.
3.  Prompt the user for a timeframe.
4.  Acknowledge and use the Compute Trend Analysis tool to analyze the information.

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

-   **Conversational topic**

Compute Trend Analysis

-   **Scripts**

Get Task Trends Config

Get Time Gap


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_analyze\_trnds

</td></tr><tr><td>

Data access roles

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_analyze\_trnds

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

Analyze task trends

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

