---
title: Universal Request departmental ticket creator AI agent
description: Automates the routing of universal requests to appropriate departmental ticketing systems by analyzing department predictions and creating properly configured HR cases or IT incidents with all necessary field mappings and reference tracking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/esm-uni-universal-request-departmental-ticket-creator-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Employee Service Management AI agents, Employee Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Universal Request departmental ticket creator AI agent

Automates the routing of universal requests to appropriate departmental ticketing systems by analyzing department predictions and creating properly configured HR cases or IT incidents with all necessary field mappings and reference tracking.

## Workflow

The agent helps users complete tasks related to universal request departmental ticket creator.

1.  Identify the department.
2.  Create the ticket.
3.  Return the result.

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

Create HR case for UR

Create incident for UR

UR Departmental service set identifier


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal

</td></tr><tr><td>

Data access roles

</td><td>

platform\_ml\_read, sn\_gaf.data\_viewer, sn\_gaf.data\_writer, sn\_uni\_req.universal\_request\_read, sn\_uni\_req.universal\_request\_write, sn\_ur\_ai\_agents.universal\_request\_read, sn\_uxc\_gen\_ai.platform\_ai\_field\_predictor

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

Universal Request Router

</td></tr></tbody>
</table>Learn more about Employee Service Management at [Employee Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-service-management-overview.md).

**Parent Topic:**[Employee Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/esm-ai-agents-overview.md)

