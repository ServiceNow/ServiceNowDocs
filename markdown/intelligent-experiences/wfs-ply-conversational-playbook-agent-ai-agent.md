---
title: Conversational playbook AI agent
description: This AI agent runs and manages playbook executions through natural conversation. It determines whether a playbook is already running for a given record, and then either resumes that execution or starts a new one. It also launches the playbook widget so that the playbook is rendered directly in the chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wfs-ply-conversational-playbook-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-16"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Creator AI agents, ServiceNow Otto for Creator, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Conversational playbook AI agent

This AI agent runs and manages playbook executions through natural conversation. It determines whether a playbook is already running for a given record, and then either resumes that execution or starts a new one. It also launches the playbook widget so that the playbook is rendered directly in the chat.

## Workflow

The agent starts, resumes, and displays a playbook for a record through a conversation with the user.

1.  Read the playbook and playbook experience identifiers from the trigger context. If no playbook is specified, tell the user and end the conversation.
2.  Retrieve the trigger table for the specified playbook to determine which table holds the parent record. If the playbook can't be found, report the issue and end the conversation.
3.  Identify the parent record for the playbook, either from a record identifier in the user's message or from the record that the user is currently viewing.
4.  If no valid record is found, ask the user whether to provide a record identifier or to use the record generator. Prompt the user again if the identifier can't be matched.
5.  Launch the playbook widget with the parent table, parent record, and playbook details so that the playbook is rendered in the conversation.

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

Find Playbook Parent Record

Get Playbook Trigger Table

Launch Playbook Widget


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

playbook.agent\_user

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Not defined.

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

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Otto for Creator AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-creator-ai-agents-overview.md)

