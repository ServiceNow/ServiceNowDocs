---
title: Data and policy configuration AI agent
description: This AI agent manages the data and policy configuration for AI on the platform. It retrieves the list of privacy policies, data patterns, data sharing, and data overflow processing details and displays it to the user. It also handles opt-in and opt-out requests for data sharing and data overflow processing \(also known as Azure Data Bursting or cloud bursting\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-data-and-policy-configuration-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Data and policy configuration AI agent

This AI agent manages the data and policy configuration for AI on the platform. It retrieves the list of privacy policies, data patterns, data sharing, and data overflow processing details and displays it to the user. It also handles opt-in and opt-out requests for data sharing and data overflow processing \(also known as Azure Data Bursting or cloud bursting\).

## Workflow

The agent requires user confirmation before making changes and validates the Data Steward role.

1.  Analyze the user's request to determine the action. If the admin's query is ambiguous between data sharing and data overflow processing, ask for clarification.
2.  View and summarize privacy policies.
3.  View and summarize data sharing details.
4.  View and summarize data overflow processing details.
5.  Answer related queries.
6.  Update data sharing.
7.  Update data overflow processing.
8.  Navigate to the privacy section page.

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

-   **Scripts**

Get Privacy Page Links

Update Data Overflow Processing

Update Data Sharing Opt Out

View Data Overflow Processing configuration

View Data sharing configuration

View Privacy Policy data


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_na\_center.nac\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_na\_center.nac\_admin, sn\_na\_center.nac\_user, sn\_generative\_ai.data\_steward

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

Multilingual and Policy Settings Manager

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

