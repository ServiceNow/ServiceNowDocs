---
title: UI builder AI agent
description: This agent helps users edit pages and answer questions within the ServiceNow UI Builder editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-uig-ui-builder-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Creator AI agents, ServiceNow Otto for Creator, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# UI builder AI agent

This agent helps users edit pages and answer questions within the ServiceNow UI Builder editor.

## Workflow

1.  Get the user's request \(or pick it up from the initial mission context\).
2.  If the user wants to make changes to their page, take control of the editor, perform the requested operations, return editor control, and summarize what changed.
3.  If the user is asking a question, search product documentation and the component library, then present an answer.
4.  Ask if the user has additional requests and repeat.

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

Add client state parameter

Add component

Add component event handler

Answer questions with product documentation search

Delete client state parameter

Delete component

Delete component event handler

Get component definition

Get list recipe

Page analyzer

Reacquire editor control

Record page recipe

Return editor control

Search component library

Update component input property

Update component preset

Update layout


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

ui\_builder\_admin

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

Not applicable.

</td></tr></tbody>
</table>Learn more about ServiceNow Otto for Creator at [ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator-landing.md).

**Parent Topic:**[ServiceNow Otto for Creator AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-creator-ai-agents-overview.md)

