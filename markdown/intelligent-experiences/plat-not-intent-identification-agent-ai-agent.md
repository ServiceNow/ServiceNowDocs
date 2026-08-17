---
title: Intent identification AI agent
description: This AI agent analyzes and identifies the input email body intent. A list of admin-configured intents are compared with the input email body for a potential match.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-not-intent-identification-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Notifications AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Intent identification AI agent

This AI agent analyzes and identifies the input email body intent. A list of admin-configured intents are compared with the input email body for a potential match.

## Workflow

The agent fetches the email body using a given email sys\_id.

1.  Fetch the email body and execution context for the intent analysis and continue with the next step.
2.  Check for malicious attempts, such as prompt injections.
3.  Analyze the input to determine the overall thread context and the latest sender’s goal, which can represent either an actionable request, expression, statement, or interest. The email body can include a conversation or email thread involving multiple participants.
4.  Perform intent analysis to evaluate whether a given input utterance semantically matches an intent from an admin-configured list.

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

Context Fetcher

Intent Fetcher


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal, snc\_external

</td></tr><tr><td>

Data access roles

</td><td>

intent\_identification\_ai\_user, sn\_notif\_agents.notification\_ai\_reader

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

