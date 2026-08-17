---
title: Translation settings AI agent
description: This AI agent handles translation settings and status inquiries for AI multilingual services. Users may refer to native translation as "NT" and Dynamic Translation as "DT."
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-translation-settings-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Translation settings AI agent

This AI agent handles translation settings and status inquiries for AI multilingual services. Users may refer to native translation as "NT" and Dynamic Translation as "DT."

## Workflow

The agent retrieves current native translation and Dynamic Translation states, enables or disables native translation, and enables or disables Dynamic Translation. It does not handle language configuration per provider. That is managed by the language configuration AI agent.

1.  Determine the requested action:
    -   View overall translation status
    -   View native translation status only
    -   View Dynamic Translation status only
    -   Enable or disable native translation
    -   Enable or disable Dynamic Translation
2.  If the user wants to view status, display the translation status.
3.  If the user wants to enable or disable translation, get the current state. Prompt the user for confirmation.
4.  Execute the requested change.

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

Get Translation Status

Toggle Dynamic Translation

Toggle Native Translation


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_na\_center.nac\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_na\_center.nac\_user, sn\_na\_center.nac\_admin

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

