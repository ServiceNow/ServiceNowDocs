---
title: Email generator AI agent
description: This AI agent composes and sends emails \(including new messages or replies\) based on the provided context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-not-email-generator-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Notifications AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Email generator AI agent

This AI agent composes and sends emails \(including new messages or replies\) based on the provided context.

## Workflow

The agent can either send the email or save it as a draft.

1.  Based on the context provided, analyze the context and determine the intended action \(either send email or save a draft\).
2.  Analyze the context to determine the type of the email: either New or Reply.
3.  Verify that all required parameters corresponding to the determined action and type are explicitly present in the provided input or current conversation context. For example, recipient information and email sys\_id.
4.  Determine the primary goal and business-appropriate purpose for the email.
5.  Construct the email.
6.  Execute the final action with all inputs.

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

Save Email Draft

Send Email


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_external, snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

email\_generator\_ai\_user, sn\_notif\_agents.email\_generator

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

