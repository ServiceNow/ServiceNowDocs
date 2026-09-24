---
title: Image to task plan template AI agent
description: This AI agent asks the user to upload an image, extracts the task dependencies from it, and returns the result as JSON.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/csm-image-to-task-plan-template-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Customer Service Management AI agents, Customer Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Image to task plan template AI agent

This AI agent asks the user to upload an image, extracts the task dependencies from it, and returns the result as JSON.

## Workflow

The agent extracts a list of tasks and their dependencies from an uploaded image.

1.  Upload the file automatically, without asking the user to upload it or showing the attachment ID in the conversation.
2.  Extract the tasks and their dependencies from the uploaded file.
3.  Display the extracted tasks, showing which tasks depend on one or more other tasks.

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

-   **Script**

Extract JSON From Image

-   **Conversational Topic**

Upload File


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_task\_plan.admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_task\_plan.admin

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

Design Telecom Order Fulfilment Template

</td></tr></tbody>
</table>**Parent Topic:**[Customer Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/csm-ai-agents-overview.md)

