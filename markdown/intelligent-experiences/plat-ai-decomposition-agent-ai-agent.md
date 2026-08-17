---
title: Decomposition AI agent
description: This AI agent takes resolution steps as input, and then analyzes and breaks down each resolution step into a clear, structured set of smaller, actionable substeps. It then creates records based on user preference. This enables precise execution, improves task clarity, and supports automation and auditability of resolution workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-decomposition-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Decomposition AI agent

This AI agent takes resolution steps as input, and then analyzes and breaks down each resolution step into a clear, structured set of smaller, actionable substeps. It then creates records based on user preference. This enables precise execution, improves task clarity, and supports automation and auditability of resolution workflows.

## Workflow

The agent retrieve table configuration, decompose the resolution plan into actionable substeps, create the records and to save the summary in the parent record. It takes resolution steps as input. It does not generate resolution steps on its own.

1.  Retrieve the table action policy XML that defines which tables can be acted on autonomously and which require supervision.
2.  Retrieve resolution steps from memory.
3.  Decompose the steps.
4.  Group actionable steps into autonomous and supervised categories. Proceed automatically with autonomous steps. For supervised steps, wait for user input before executing.
5.  Finalize the execution set.
6.  Create the record.
7.  Save activity notes.

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

Create record

Get actionable tables from skill config

Get Fields from Table

Save activity notes

-   **Generative AI skill**

Step Decomposer


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_decomposition\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_uxc\_gen\_ai.platform\_ai\_decomposition\_agent, sn\_hr\_core.case\_writer

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

Generate resolution plans

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

