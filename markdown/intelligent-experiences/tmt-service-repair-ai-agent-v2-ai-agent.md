---
title: Service repair AI agent V2
description: The agent reviews the results of a service test and creates a repair task when the test fails. It summarizes the diagnostic task, the overall test result, and any repair tasks created, and writes that summary to the work notes of the task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-service-repair-ai-agent-v2-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Service repair AI agent V2

The agent reviews the results of a service test and creates a repair task when the test fails. It summarizes the diagnostic task, the overall test result, and any repair tasks created, and writes that summary to the work notes of the task.

## Workflow

The agent acts on the results of a service test and records the outcome in the work notes of the task.

1.  Receive the task details, the collection and validation statuses, and the test results from the orchestrator.
2.  Build the summary from the collection or validation response alone when either status reports a failure or a stop.
3.  Create a repair task by using the primary task ID when the test results report a failure.
4.  Collect the hyperlink summary for the repair tasks created.
5.  Format the summary with the diagnostic task number, the overall test result, and the repair tasks created.
6.  Update the work notes of the task with the summary.

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

-   **Flow Action**

Create the repair task for the test runs

-   **Script**

Update task work notes


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   itil
-   sn\_sprb\_mgmt.agent
-   sn\_tmt\_agentic\_ai.test\_and\_repair\_telecom\_service\_ai\_agent

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

Service Test and Repair

</td></tr></tbody>
</table>Learn more about Customer Service Problem Management at [Customer Service Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/cspm-landing-page.md).

**Parent Topic:**[Customer Service Problem Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/cspm-ai-agents-overview.md)

