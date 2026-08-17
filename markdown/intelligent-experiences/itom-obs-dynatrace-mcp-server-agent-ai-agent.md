---
title: Dynatrace MCP server AI agent
description: This AI agent provides the details for a given alert by querying the Dynatrace API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-obs-dynatrace-mcp-server-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [IT Operations Management AI agents, IT Operations Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Dynatrace MCP server AI agent

This AI agent provides the details for a given alert by querying the Dynatrace API.

## Workflow

The agent fetches the problem report for a Dynatrace alert.

1.  Retrieve problem details.
2.  Extract the context of the problem.
3.  Enrich entity information.
4.  Perform scan analysis.
5.  Summarize results.
6.  Log the investigation.

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

Agent roles \(ACLs\)

</td><td>

evt\_mgmt\_operator

</td></tr><tr><td>

Data access roles

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

Analyze alert impact

</td></tr></tbody>
</table>Learn more about IT Operations Management at [IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/r_ITOMApplications.md).

**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-ai-agents-overview.md)

