---
title: Registration error monitor AI agent
description: This AI agent checks a registration number and connection against the Service Exchange error table, and then provides a detailed summary of any reported Service Exchange errors. This summary helps users or other AI agents make informed decisions and take appropriate action to resolve registration issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/srvc-ex-registration-error-monitor-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Service Exchange AI agents, Service Exchange, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Registration error monitor AI agent

This AI agent checks a registration number and connection against the Service Exchange error table, and then provides a detailed summary of any reported Service Exchange errors. This summary helps users or other AI agents make informed decisions and take appropriate action to resolve registration issues.

## Workflow

The agent helps a user check a registration number and review any related Service Exchange errors.

1.  Ask the user for the registration number to check, in the format REG followed by seven digits, for example REG0010010.
2.  Look up the given registration number and connection in the Service Exchange error table.
3.  Summarize any Service Exchange errors found for that registration number and connection.
4.  Present the summary to the user so they can decide on next steps.

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

-   **Scripts**

Find Company

Show Service Exchange errors link

Verify registration


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_sb.admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_sb.admin

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

Service Exchange Onboarding

</td></tr></tbody>
</table>**Parent Topic:**[Service Exchange AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/srvc-ex-ai-agents-overview.md)

