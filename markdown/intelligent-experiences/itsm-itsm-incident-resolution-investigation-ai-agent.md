---
title: ITSM incident resolution investigation AI agent
description: This AI agent retrieves incident details and can add attached knowledge articles and additional comments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itsm-itsm-incident-resolution-investigation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [IT Service Management AI agents, IT Service Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# ITSM incident resolution investigation AI agent

This AI agent retrieves incident details and can add attached knowledge articles and additional comments.

## Workflow

The agent determines the issue with the incident, searches for potential solutions, and comes up with a plan to solve the issue.

1.  Get the details of the incident.
2.  Find a list of similar incidents to understand how they were resolved.
3.  Find a list of relevant knowledge articles, based on the short description of the incident.
4.  Generate an incident resolution plan and add it to the incident's work notes.

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

Add a resolution plan to incident's work notes

Get details of Incident

-   **Search retrievals**

Get relevant knowledge articles

Get similar incidents


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_service\_desk\_agent, itil

</td></tr><tr><td>

Data access roles

</td><td>

sn\_service\_desk\_agent, itil

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Enable the AI agent for the ServiceNow Otto panel.

</td></tr><tr><td>

Used in agentic workflows

</td><td>

ITSM Agent Zero

</td></tr></tbody>
</table>Learn more about IT Service Management at [IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md).

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

