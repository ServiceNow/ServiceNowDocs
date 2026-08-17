---
title: Parts audit AI agent
description: This AI agent assists technicians in conducting thorough parts validation only for work order tasks. It streamlines the process of verifying and reporting parts usage, ensuring accuracy and accountability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/fsm-parts-audit-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Field Service Management AI agents, Field Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Parts audit AI agent

This AI agent assists technicians in conducting thorough parts validation only for work order tasks. It streamlines the process of verifying and reporting parts usage, ensuring accuracy and accountability.

## Workflow

The agent helps users complete tasks related to parts audit agent.

1.  Use the appropriate tool to fetch the work notes with record number from context.
2.  Extract the model details, such as model name, quantity, and so on.
3.  Check for assets.
4.  Match usable and removable assets.
5.  Present the user with a summary and wait for confirmation.
6.  Perform requested operations.
7.  Present the user with a final message.

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

Fetch work notes

Remove part action

Use part action

-   **Generative AI skills**

Removable asset matching tool

Usable asset matching tool


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

wm\_agent

</td></tr><tr><td>

Data access roles

</td><td>

wm\_agent

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

Validate parts

</td></tr></tbody>
</table>Learn more about  at [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ext-cont-connectors-landing-page.md).

**Parent Topic:**[Field Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/fsm-ai-agents-overview.md)

