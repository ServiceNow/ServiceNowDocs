---
title: Dispute communication AI agent
description: The agent drafts a customer email about a card dispute outcome. It chooses the message template based on the dispute's final action, fills in the relevant transaction and merchant details, and adjusts the tone to match the template's intended message.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/fso-dispute-communication-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 1
breadcrumb: [Financial Services Operations AI Agents, Financial Services Operations, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Dispute communication AI agent

The agent drafts a customer email about a card dispute outcome. It chooses the message template based on the dispute's final action, fills in the relevant transaction and merchant details, and adjusts the tone to match the template's intended message.

## Workflow

The agent helps prepare the customer-facing email for a resolved card dispute.

1.  Retrieve the dispute task's full details using the given task ID.
2.  Find the email template that matches the dispute's final action.
3.  Fill in the template with the dispute's transaction, merchant, and customer details.
4.  Adjust the tone and phrasing of the filled-in message to match the template's intended tone, while keeping its structure and formatting.
5.  Create an email draft record with the finished content and report the outcome.

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

Fetch card disputes task context details

Generate dispute communication email draft record

-   **Search retrievals**

Get email templates


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   sn\_bom\_credit\_card.dispute\_agent
-   sn\_bom\_credit\_card.dispute\_agent\_connector

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_bom\_credit\_card.dispute\_agent
-   sn\_bom\_credit\_card.dispute\_agent\_connector

</td></tr><tr><td>

Triggers

</td><td>

Dispute communication task

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/fso-ai-agents-overview.md)

