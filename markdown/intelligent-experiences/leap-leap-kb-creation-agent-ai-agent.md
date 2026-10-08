---
title: LEAP KB Creation Agent AI agent
description: The LEAP KB Creation agent creates draft knowledge base articles from the resolution steps of a LEAP automation opportunity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/leap-leap-kb-creation-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 1
breadcrumb: [AIOps and Leap AI agents, AIOps and AIOps Leap, AI agents library, AI assets, Enable AI experiences]
---

# LEAP KB Creation Agent AI agent

The LEAP KB Creation agent creates draft knowledge base articles from the resolution steps of a LEAP automation opportunity.

## Workflow

The agent helps the user create a draft knowledge base article for an automation opportunity.

1.  Identify the automation opportunity number from the request.
2.  Create a draft knowledge base article from the resolution steps of the automation opportunity.
3.  Confirm that the article was created, or report the error details if creation failed.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

LEAP Create KB Article


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_itom\_leap.artifact\_creator\_agent

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

LEAP Autonomous Agent

</td></tr></tbody>
</table>**Parent Topic:**[AIOps and Leap AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aiops-ai-agents-overview.md)

