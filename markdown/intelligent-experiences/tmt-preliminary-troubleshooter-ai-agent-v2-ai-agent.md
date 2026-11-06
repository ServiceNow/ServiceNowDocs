---
title: Preliminary troubleshooter AI Agent V2
description: The agent triages a task by retrieving relevant knowledge articles and similar historical tasks, and consolidates them into a resolution plan with recommended next steps. It writes the plan, along with any customer payment information, to the work notes of the task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-preliminary-troubleshooter-ai-agent-v2-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Preliminary troubleshooter AI Agent V2

The agent triages a task by retrieving relevant knowledge articles and similar historical tasks, and consolidates them into a resolution plan with recommended next steps. It writes the plan, along with any customer payment information, to the work notes of the task.

## Workflow

The agent builds a consolidated resolution plan for a task and records it in the work notes.

1.  Receive the task details, the task validation status, and the payment status from the orchestrator.
2.  Build the summary from the validation response alone when the task validation status is STOP.
3.  Retrieve the knowledge articles that match the short description of the task.
4.  Retrieve similar historical tasks and the resolution approaches that resolved them.
5.  Generate a resolution plan from the knowledge articles and the similar tasks, and report that no plan could be produced when neither is available.
6.  Format the consolidated summary with the payment status and the recommended next steps.
7.  Write the summary to the work notes of the task and report the result to the orchestrator.

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

Update task work notes

-   **Tool**

Get Similar Tasks

Get relevant knowledge articles


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

Not defined.

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

Preliminary troubleshooter

</td></tr></tbody>
</table>Learn more about Customer Service Problem Management at [Customer Service Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/cspm-landing-page.md).

**Parent Topic:**[Customer Service Problem Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/cspm-ai-agents-overview.md)

