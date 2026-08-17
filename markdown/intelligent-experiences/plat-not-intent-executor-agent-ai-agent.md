---
title: Intent executor AI agent
description: This AI agent executes admin-defined actions, such as workflows or creating reply responses based on matched intent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-not-intent-executor-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Notifications AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Intent executor AI agent

This AI agent executes admin-defined actions, such as workflows or creating reply responses based on matched intent.

## Workflow

The agent cannot analyze or compare the intent, nor can it generate an email or email draft itself.

1.  Find intent matches.
2.  Extract values from input and create JSON.
3.  Validate the execution payload JSON.
4.  After successfully executing all subflow actions, fetch the email actions that match the intent or fetch the default email actions if there is no intent match.
5.  Generate email.

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

Email Action Fetcher

SubFlow Action Executor

SubFlow Action Fetcher


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_external, snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

sn\_notif\_agents.intent\_executor

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

Intent to Action

</td></tr></tbody>
</table>Learn more about Notifications in [Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notifications.md).

**Parent Topic:**[Notifications AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-notifications-ai-agents-overview.md)

