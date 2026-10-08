---
title: Artifact creation agent AI agent
description: The Artifact creation agent helps users create and view artifacts for an automation opportunity, such as a problem record, a knowledge base article, or a playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/leap-artifact-creation-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 1
breadcrumb: [AIOps and Leap AI agents, AIOps and AIOps Leap, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Artifact creation agent AI agent

The Artifact creation agent helps users create and view artifacts for an automation opportunity, such as a problem record, a knowledge base article, or a playbook.

## Workflow

The agent helps the user create or view artifacts for an automation opportunity.

1.  Check whether an automation opportunity number is available.
2.  Start the artifact creation conversation for that automation opportunity.
3.  Guide the user to create or view a problem record, knowledge base article, or playbook for the opportunity.
4.  End the workflow when the conversation is complete.

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

-   **Tool**

artifact creation topic


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

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

LEAP agent

</td></tr></tbody>
</table>**Parent Topic:**[AIOps and Leap AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aiops-ai-agents-overview.md)

